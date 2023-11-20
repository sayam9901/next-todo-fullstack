# next-todo-fullstack
this is external files needed for the project submission
import React from 'react'
import { useRouter } from 'next/router'


const AboutName = () => {
  const router = useRouter()
  const details = [  { id : 1, name: 'Yash', role: 'Senior Developer'},
  { id : 2, name: 'Vaibhav', role: 'Backend Developer'},
  { id : 3, name: 'Suresh', role: 'Frontend Developer'}]
   let data;
  if(router.query.Developer){
    data = details.find(item => item.id == router.query.Developer) 
  }
  console.log(data)
  console.log(typeof(router.query.Developer))
  return (
  <>
  {data && <p>{data.name} --- {data.role}</p>}
  </>
  )
}

export default AboutName
