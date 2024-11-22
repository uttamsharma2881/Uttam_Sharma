/* Calendar grid */
.calendar {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: 1rem;
}

.day {
    background-color: #f8f9fa;
    border: 1px solid #dee2e6;
    padding: 20px;
    text-align: center;
}

/* Highlight today */
.today {
    background-color: #007bff;
    color: white;
    z-index: 10;
}

/* Event bubble */
.event {
    background-color: #ffcc00;
    padding: 5px;
    text-align: center;
    
   
}

.event-content {
    display: none;
    position: relative;
    background-color: var(--tertiary-color);
    top: 50%;
    color: var(--secondary-color);
    min-width: 180px;
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.1);
    z-index: 10;
    border-radius: 8px;
    padding: 5px 10px;

    white-space: nowrap;
    cursor:pointer;

}

.event:hover .event-content {
  display: block;
  
}

.upEvent-card{
  background-color: whitesmoke;
  margin: 2px 0;
  padding: 1rem;
}

.upEvent-card:hover{
  background: linear-gradient(135deg, var(--tertiary-color), var(--dark-primary-color));
  color:var(--secondary-color);
}



.cal-navigation {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    grid-template-rows: auto;
  }
  
  .cal-nav{
    flex: 1;
  }
  
  .cal-nav.prev {
    grid-column: 1;
  }
  .cal-nav.month {
    grid-column: 2;
  }
  .cal-nav.next {
    grid-column: 3;
  }

/* Responsive adjustments */
@media (max-width: 768px) {
    /* Switch to 2 or 3 columns on smaller screens */
    .calendar {
        display: none;
    }

    .day {
        padding: 15px;
        font-size: 0.9rem;
    }

    .event-content {
        min-width: 140px; /* Smaller width for smaller screens */
        padding: 5px 8px;
        font-size: 0.85rem;
    }

    
.cal-navigation{
    flex-direction: column;
  }
  
    .cal-nav.month {
      grid-column: span 3;
      flex: 1;
      text-align: center;
    }
    .cal-nav.prev,
    .cal-nav.next {
      order: 2;
      flex: .5;
      margin: 0 15px;
      
    }
}



