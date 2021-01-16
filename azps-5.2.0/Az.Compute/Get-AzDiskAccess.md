---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295277"
---
# <span data-ttu-id="57e8a-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="57e8a-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="57e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="57e8a-103">Ruft die Eigenschaften von Datenträgerzugriffen ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="57e8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57e8a-104">SYNTAX</span></span>

### <span data-ttu-id="57e8a-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="57e8a-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57e8a-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="57e8a-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e8a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="57e8a-108">Das **Cmdlet "Get-AzDiskAccess"** ruft die Eigenschaften von Datenträgerzugriffen ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="57e8a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="57e8a-110">Beispiel 1: Verwenden des Standardparametersets</span><span class="sxs-lookup"><span data-stu-id="57e8a-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="57e8a-111">Dieser Befehl ruft die Eigenschaften einer Datenträgerzugriffsressource mit dem Namen "DiskAccess01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="57e8a-112">Beispiel 2: Get-AzDiskAccess nach Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="57e8a-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="57e8a-113">Dieser Befehl ruft die Eigenschaften aller Datenträgerzugriffe in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="57e8a-114">Beispiel 3: Abrufen des Zugriffs auf den Datenträger</span><span class="sxs-lookup"><span data-stu-id="57e8a-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="57e8a-115">Dieser Befehl ruft die Eigenschaften aller Datenträgerzugriffe unter dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="57e8a-116">Beispiel 4: Den ganzen Datenträgerzugriff mit Platzhalterzeichen erhalten</span><span class="sxs-lookup"><span data-stu-id="57e8a-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="57e8a-117">Dieser Befehl ruft die Eigenschaften aller Datenträgerzugriffe unter dem Abonnementnamen ab "DiskAccessMicrosoft" ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="57e8a-118">Beispiel 5: Zugreifen auf Datenträger mithilfe von ResourceId.</span><span class="sxs-lookup"><span data-stu-id="57e8a-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="57e8a-119">Dieser Befehl ruft die Eigenschaften eines Datenträgerzugriffs mit der angegebenen ResourceId ab.</span><span class="sxs-lookup"><span data-stu-id="57e8a-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="57e8a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57e8a-120">PARAMETERS</span></span>

### <span data-ttu-id="57e8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e8a-121">-DefaultProfile</span></span>
<span data-ttu-id="57e8a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57e8a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e8a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="57e8a-123">-Name</span></span>
<span data-ttu-id="57e8a-124">Gibt den Namen eines Datenträgerzugriffs an.</span><span class="sxs-lookup"><span data-stu-id="57e8a-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="57e8a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e8a-125">-ResourceGroupName</span></span>
<span data-ttu-id="57e8a-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="57e8a-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="57e8a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57e8a-127">-ResourceId</span></span>
<span data-ttu-id="57e8a-128">Ressourcen-ID für den Datenträgerzugriff.</span><span class="sxs-lookup"><span data-stu-id="57e8a-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e8a-129">CommonParameters</span></span>
<span data-ttu-id="57e8a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e8a-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e8a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e8a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57e8a-132">INPUTS</span></span>

### <span data-ttu-id="57e8a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="57e8a-133">System.String</span></span>

## <span data-ttu-id="57e8a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57e8a-134">OUTPUTS</span></span>

### <span data-ttu-id="57e8a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="57e8a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="57e8a-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="57e8a-136">NOTES</span></span>

## <span data-ttu-id="57e8a-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="57e8a-137">RELATED LINKS</span></span>
