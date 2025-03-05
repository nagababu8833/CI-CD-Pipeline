Here's a **smaller** Terraform file to create an **Azure Resource Group** and a **Virtual Network**:  

### **main.tf**  
```hcl
provider "azurerm" {
  features {}
}

resource "azurerm_resource_group" "rg" {
  name     = "myResourceGroup"
  location = "East US"
}

resource "azurerm_virtual_network" "vnet" {
  name                = "myVnet"
  location            = azurerm_resource_group.rg.location
  resource_group_name = azurerm_resource_group.rg.name
  address_space       = ["10.0.0.0/16"]
}
```

### **Steps to Apply:**
1. Save as `main.tf`
2. Run:
   ```sh
   terraform init
   terraform apply -auto-approve
   ```

This is a minimal setup. Let me know if you need modifications! 🚀
