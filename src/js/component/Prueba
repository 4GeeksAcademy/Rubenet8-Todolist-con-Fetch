// Import
import React, { useEffect, useState } from "react";

// Export
export const ExampleFetchComplex = () => {
    const [characters, setCharacters] = useState([])
    const base_url = 'https://swapi.tech/api';


    const getCharacters = async () => {
        const uri = `${base_url}/people`
        const options = {
            method: 'GET'
        }

        const response = await fetch(uri, options)
        if (!response.ok) {
            console.log('Error:', response.status, response.statusText)
            return;
        }

        const data = await response.json()

        console.log('Soy el contenido de data', data);
        setCharacters(data.results)
    }

    useEffect(() => {
        getCharacters();
    }, [])

    return (
        <div className="container">
            <h1 className="text-center text-success">Example Fetch() Complex</h1>
            <ul className="list-group">
                {characters.map((iterator) =>
                    <li key={iterator.uid} className="list-group-item">{iterator.name}</li>
                )}
            </ul>
        </div>
    )
}