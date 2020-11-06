---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499361"
---
# <span data-ttu-id="fb3a2-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fb3a2-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="fb3a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3a2-103">Gibt Informationen zu Azure SQL-Datenbankinstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3a2-104">SYNTAX</span></span>

### <span data-ttu-id="fb3a2-105">GetInstanceByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb3a2-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb3a2-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb3a2-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb3a2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb3a2-107">DESCRIPTION</span></span>
<span data-ttu-id="fb3a2-108">Das Cmdlet " **Get-AzureRmSqlInstance** " gibt Informationen zu mindestens einem Azure SQL-verwalteten Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="fb3a2-109">Geben Sie den Namen einer Instanz an, um Informationen nur für diese Instanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="fb3a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb3a2-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3a2-111">Beispiel 1: Abrufen aller Instanzen, die einer Ressourcengruppe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="fb3a2-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="fb3a2-112">Dieser Befehl ruft Informationen zu allen Instanzen ab, die der Ressourcengruppe ResourceGroup01 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="fb3a2-113">Beispiel 2: Abrufen von Informationen zu einer Instanz</span><span class="sxs-lookup"><span data-stu-id="fb3a2-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="fb3a2-114">Dieser Befehl ruft Informationen zur Instanz mit dem Namen managedInstance1 ab.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="fb3a2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb3a2-115">PARAMETERS</span></span>

### <span data-ttu-id="fb3a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3a2-116">-DefaultProfile</span></span>
<span data-ttu-id="fb3a2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fb3a2-118">-Name</span></span>
<span data-ttu-id="fb3a2-119">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="fb3a2-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb3a2-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3a2-122">CommonParameters</span></span>
<span data-ttu-id="fb3a2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3a2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3a2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3a2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb3a2-125">INPUTS</span></span>

### <span data-ttu-id="fb3a2-126">Keine</span><span class="sxs-lookup"><span data-stu-id="fb3a2-126">None</span></span>

## <span data-ttu-id="fb3a2-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb3a2-127">OUTPUTS</span></span>

### <span data-ttu-id="fb3a2-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fb3a2-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fb3a2-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb3a2-129">NOTES</span></span>

## <span data-ttu-id="fb3a2-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb3a2-130">RELATED LINKS</span></span>
