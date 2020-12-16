# Contoso Ship Manager - Demo Application

> This is a short sample code for Microsoft Learn

## Features

This project is a simple harbor control application to track ships. It consists on a front-end and a back-end part.

## Getting Started

### Prerequisites

- Node.js version 8 for the Frontend
- Node.js version 12 or later for the backend
- Docker and Docker Compose
- MongoDB

### Installation & Quickstart

#### Running stand alone

The application is divided into two main directories: `frontend` and `backend` each one with their respective codes and infrastructure files.

__Front End__: Created using Vim. Just go into the directory, type `npm install` to install all dependencies and then `npm run serve`. You can also build the image from the Dockerfile in the same directory

__Front End__: Created with TypeScript. Just go into the directory, type `npm install` to install all dependencies and then `npm run build:start` to run the app or `npm run start:debug` to start in debug mode (tsc watch and logging). You can also build the image from the Dockerfile in the same directory

#### Application hosted image

There's a hosted image of this application available at the MCR (Microsoft Container Registry) in the following address: `mcr.microsoft.com/mslearn/samples/contoso-ship-manager`

You can pull this image using `docker pull` and run it locally using `docker run`.

### Environment Variables

The backend portion requires environment variables to run, those are:

- DATABASE_MONGODB_URI: URI of the MongoDB database
- DATABASE_MONGODB_DBNAME: MongoDB database name
