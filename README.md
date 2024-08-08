# first-project
Component folder:
-----data.jsx-------- 
import {FiFlag, FiShield} from 'react-icons/fi'
import {BiWalletAlt, BiKey} from 'react-icons/bi'
import {FaPlane} from 'react-icons/fa'
import {RiCustomerServiceFill} from 'react-icons/ri'
export const Data = [
    {
        icon:<FiFlag/>,
        title:'HostPassword Scanner',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
    {
        icon:<BiWalletAlt/>,
        title:'Digital Wallet',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
    {
        icon:<BiKey/>,
        title:'Advanced Encryption',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
    {
        icon:<FaPlane/>,
        title:'Travel Mode',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
    {
        icon:<FiShield/>,
        title:'Total privacy',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
    {
        icon:<RiCustomerServiceFill/>,
        title:'Unrivaled Support',
        description:'Receive alerts for compromised website and this is, Receive alerts for compromised website and this is'
    },
]

export const FooterData = [
    {
        category:'About',
        links:[
            {
                link:'Pricing & Packaging',
                to:'/'
            },
            {
                link:'Contact Us',
                to:'/'
            },
            {
                link:'Software Company',
                to:'/'
            },
            {
                link:'SaaS Companies',
                to:'/'
            },
            {
                link:'Startups',
                to:'/'
            },
            {
                link:'Games',
                to:'/'
            },
            {
                link:'Application',
                to:'/'
            },
            {
                link:'Ecommerce',
                to:'/'
            }
        ]
    },
    {
        category:'Company',
        links:[
            {
                link:'Help',
                to:'/'
            },
            {
                link:'Contact Us',
                to:'/'
            },
            {
                link:'Privacy',
                to:'/'
            },
            {
                link:'Check Our Story',
                to:'/'
            },
            {
                link:'Work with us',
                to:'/'
            },
            {
                link:'Press',
                to:'/'
            },
            {
                link:'Apps',
                to:'/'
            },
            {
                link:'Blog',
                to:'/'
            }
        ]
    },
    {
        category:'Features',
        links:[
            {
                link:'Wallet',
                to:'/'
            },
            {
                link:'Payment System',
                to:'/'
            },
            {
                link:'Multiple',
                to:'/'
            },
            {
                link:'Business',
                to:'/'
            },
            {
                link:'Merchants',
                to:'/'
            },
            {
                link:'Micropayments',
                to:'/'
            },
            {
                link:'Invoice % Billing',
                to:'/'
            },
            {
                link:'Fraud Detection',
                to:'/'
            }
        ]
    },
    {
        category:'Platform',
        links:[
            {
                link:'Fees',
                to:'/'
            },
            {
                link:'AnyPay for Business',
                to:'/'
            },
            {
                link:'Login to AnyPay',
                to:'/'
            },
            {
                link:'AnyPay Status',
                to:'/'
            },
            {
                link:'Market Place',
                to:'/'
            },
            {
                link:'Tour',
                to:'/'
            },
            {
                link:'Become Merchant',
                to:'/'
            },
            {
                link:'Market Cap',
                to:'/'
            }
        ]
    },
    {
        category:'Resource',
        links:[
            {
                link:'Blog',
                to:'/'
            },
            {
                link:'Whitepapers',
                to:'/'
            },
            {
                link:'Webinars',
                to:'/'
            },
            {
                link:'Product Datasheets',
                to:'/'
            },
            {
                link:'Customer Case studies',
                to:'/'
            },
            {
                link:'Developer Portal',
                to:'/'
            },
            {
                link:'  Knowledge Center',
                to:'/'
            },
            {
                link:'Sandbox',
                to:'/'
            }
        ]
    },
]

------Footer.jsx------------
import React from 'react'
import { Link } from 'react-router-dom'
import './footer.scss'
import { FooterData } from './data'


const Footer = () => {
  return (
    <div className='footer'>
    {FooterData.map((props) => {
        return(
            <div className='col'>
            <h6>{props.category}</h6>
            <div className='links'>
            {props.links.map((l) => {
                return(
                    <Link key={l.to} to={l.to}>{l.link}</Link>
                )
            })}
            </div>
            </div>
        )
    })}
    </div>
  )
}

export default Footer


-------Item.jsx----
import React from 'react'

const Item = (icon, title, description) => {
  return (
        <div className='item'>
          <div className='icon'>{icon}</div>
              <h6>{title}</h6>
              <p>{description}</p>
        </div>  
  )
}

export default Item

-----NavData.jsx-------
import {FiFlag, FiShield} from 'react-icons/fi'
import {BiWalletAlt, BiKey} from 'react-icons/bi'

export const NavData = [
    {
        icon:<FiFlag/>,
        title: 'Title1',
        description: 'Lorem Ipsun dolor .....'
    },
    {
        icon:<FiShield/>,
        title: 'Title2',
        description: 'Lorem Ipsun dolor .....'
    },
    {
        icon:<BiWalletAlt/>,
        title: 'Title3',
        description: 'Lorem Ipsun dolor .....'
    },
    {
        icon:<BiKey/>,
        title: 'Title4',
        description: 'Lorem Ipsun dolor .....'
    }
]

---------Popup.jsx------------
import React, {useState} from 'react'
import './user.scss'

const Popup = () => {
    const [popup, setPopup] = useState(false)
    const showPopup = () => {
        setPopup(!popup)
    }

    const closePopup = () => {
        setPopup(false)
    }
  return (
    
<div className='popup'>

{popup ? <div className='backdrop' onClick={closePopup}></div> : null}
 
    <button type='button' onClick={showPopup}>Show Popup</button>
 {popup ? 
 <div className='card'>
     <h1>Popup</h1>
     <p>oooooooooooooooooooooooooo...</p>
     <p>oooooooooooooooooooooooooo...</p>
     <p>oooooooooooooooooooooooooo...</p>
 </div> : null
}
    </div>
  )
}

export default Popup

-----User.jsx------
import React from 'react'
import { Data } from './data'
import './user.scss'
import Item from './Item'

const User = () => {
  return (
    <div className='user'>
        {Data.map((d, i) => {
          return(
            <Item
           key={i} {...d}
            />
          )
        })}
    </div>
  )
}

export default User
