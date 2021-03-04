---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938888"
---
# <span data-ttu-id="eb145-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="eb145-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="eb145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb145-102">SYNOPSIS</span></span>
<span data-ttu-id="eb145-103">Hosts erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="eb145-103">Get or list hosts.</span></span>

## <span data-ttu-id="eb145-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb145-104">SYNTAX</span></span>

### <span data-ttu-id="eb145-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb145-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb145-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="eb145-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb145-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb145-107">DESCRIPTION</span></span>
<span data-ttu-id="eb145-108">Dieses Cmdlet wird eine Hostgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb145-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="eb145-109">In diesem Cmdlet werden auch alle Hostgruppen in einer Ressourcengruppe aufgeführt, wenn kein Hostgruppenname angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eb145-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="eb145-110">In diesem Cmdlet werden auch alle Hostgruppen in einem Abonnement aufgeführt, wenn weder der Name der Hostgruppe noch der Name der Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eb145-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="eb145-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb145-111">EXAMPLES</span></span>

### <span data-ttu-id="eb145-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb145-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="eb145-113">Dieser Befehl gibt eine Hostgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="eb145-113">This command returns a host group.</span></span>

### <span data-ttu-id="eb145-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eb145-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="eb145-115">Dieser Befehl gibt alle Hostgruppen in der angegebenen Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="eb145-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="eb145-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="eb145-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="eb145-117">Dieser Befehl gibt alle Hostgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="eb145-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="eb145-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb145-118">PARAMETERS</span></span>

### <span data-ttu-id="eb145-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb145-119">-DefaultProfile</span></span>
<span data-ttu-id="eb145-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb145-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb145-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="eb145-121">-InstanceView</span></span>
<span data-ttu-id="eb145-122">Erweitern Sie das zurückgegebene Objekt, um auch die Instanzansichten des Hosts auflisten zu können.</span><span class="sxs-lookup"><span data-stu-id="eb145-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb145-123">-Name</span><span class="sxs-lookup"><span data-stu-id="eb145-123">-Name</span></span>
<span data-ttu-id="eb145-124">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb145-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb145-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb145-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb145-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb145-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb145-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb145-127">-ResourceId</span></span>
<span data-ttu-id="eb145-128">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="eb145-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb145-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb145-129">CommonParameters</span></span>
<span data-ttu-id="eb145-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb145-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb145-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb145-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb145-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb145-132">INPUTS</span></span>

### <span data-ttu-id="eb145-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eb145-133">System.String</span></span>

## <span data-ttu-id="eb145-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb145-134">OUTPUTS</span></span>

### <span data-ttu-id="eb145-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="eb145-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="eb145-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb145-136">NOTES</span></span>

## <span data-ttu-id="eb145-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb145-137">RELATED LINKS</span></span>
