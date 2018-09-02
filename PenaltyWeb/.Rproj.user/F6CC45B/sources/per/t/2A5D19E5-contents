#
# This is a Shiny web application. You can run the application by clicking
# the 'Run App' button above.
#
# Find out more about building applications with Shiny here:
#
#    http://shiny.rstudio.com/
#

library(shiny)
library(leaflet)

# Define UI for application that draws a histogram
ui <- fluidPage(
  titlePanel("Title"),
  sidebarLayout(
    sidebarPanel("sidebar panel"),
    mainPanel(
              leafletOutput("mymap")
              )
    
  )
  
)

# Define server logic required to draw a histogram
server <- function(input, output) {
  output$mymap <- renderLeaflet({
    m <- leaflet() %>%
      addTiles() %>%
      setView(lng=-73.935242, lat=40.730610 , zoom=10)
    m
  })
}

# Run the application 
shinyApp(ui = ui, server = server)

