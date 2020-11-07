---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659185"
---
# <span data-ttu-id="6cf0f-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6cf0f-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="6cf0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cf0f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf0f-103">Gibt Informationen zu Azure SQL-Datenbankinstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="6cf0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cf0f-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cf0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cf0f-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf0f-106">Das Cmdlet " **Get-AzSqlInstance** " gibt Informationen zu mindestens einem Azure SQL-verwalteten Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="6cf0f-107">Geben Sie den Namen einer Instanz an, um Informationen nur für diese Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="6cf0f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cf0f-108">EXAMPLES</span></span>

### <span data-ttu-id="6cf0f-109">Beispiel 1: Abrufen aller Instanzen, die einer Ressourcengruppe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="6cf0f-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="6cf0f-110">Dieser Befehl ruft Informationen zu allen Instanzen ab, die der Ressourcengruppe ResourceGroup01 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6cf0f-111">Beispiel 2: Abrufen von Informationen zu einer Instanz</span><span class="sxs-lookup"><span data-stu-id="6cf0f-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="6cf0f-112">Dieser Befehl ruft Informationen zur Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="6cf0f-113">Beispiel 3: Abrufen aller Instanzen, die einer Ressourcengruppe zugeordnet sind, mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="6cf0f-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="6cf0f-114">Dieser Befehl ruft Informationen zu allen Instanzen ab, die der Ressourcengruppen-ResourceGroup01 zugeordnet sind, die mit "managedInstance" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="6cf0f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cf0f-115">PARAMETERS</span></span>

### <span data-ttu-id="6cf0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf0f-116">-DefaultProfile</span></span>
<span data-ttu-id="6cf0f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf0f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6cf0f-118">-Name</span></span>
<span data-ttu-id="6cf0f-119">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="6cf0f-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6cf0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cf0f-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6cf0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf0f-122">CommonParameters</span></span>
<span data-ttu-id="6cf0f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf0f-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf0f-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf0f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cf0f-125">INPUTS</span></span>

### <span data-ttu-id="6cf0f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="6cf0f-126">None</span></span>

## <span data-ttu-id="6cf0f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cf0f-127">OUTPUTS</span></span>

### <span data-ttu-id="6cf0f-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6cf0f-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="6cf0f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cf0f-129">NOTES</span></span>

## <span data-ttu-id="6cf0f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cf0f-130">RELATED LINKS</span></span>
