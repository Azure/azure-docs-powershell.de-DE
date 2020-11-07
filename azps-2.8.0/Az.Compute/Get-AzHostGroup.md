---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652174"
---
# <span data-ttu-id="6649f-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="6649f-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="6649f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6649f-102">SYNOPSIS</span></span>
<span data-ttu-id="6649f-103">Abrufen oder Auflisten von Hosts</span><span class="sxs-lookup"><span data-stu-id="6649f-103">Get or list hosts.</span></span>

## <span data-ttu-id="6649f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6649f-104">SYNTAX</span></span>

### <span data-ttu-id="6649f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="6649f-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6649f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6649f-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6649f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6649f-107">DESCRIPTION</span></span>
<span data-ttu-id="6649f-108">Dieses Cmdlet erhält eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="6649f-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="6649f-109">Dieses Cmdlet listet auch alle Hostgruppen in einer Ressourcengruppe auf, wenn kein Hostgruppen Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6649f-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="6649f-110">Dieses Cmdlet listet auch alle Hostgruppen in einem Abonnement auf, wenn weder der Name der Hostgruppe noch der Name der Ressourcengruppe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6649f-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="6649f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6649f-111">EXAMPLES</span></span>

### <span data-ttu-id="6649f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6649f-112">Example 1</span></span>
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

<span data-ttu-id="6649f-113">Dieser Befehl gibt eine Hostgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="6649f-113">This command returns a host group.</span></span>

### <span data-ttu-id="6649f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6649f-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="6649f-115">Dieser Befehl gibt alle Hostgruppen in der angegebenen Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="6649f-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="6649f-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6649f-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="6649f-117">Dieser Befehl gibt alle Hostgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="6649f-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="6649f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="6649f-118">PARAMETERS</span></span>

### <span data-ttu-id="6649f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6649f-119">-DefaultProfile</span></span>
<span data-ttu-id="6649f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6649f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6649f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6649f-121">-Name</span></span>
<span data-ttu-id="6649f-122">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="6649f-122">The name of the host group.</span></span>

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

### <span data-ttu-id="6649f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6649f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6649f-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6649f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6649f-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6649f-125">-ResourceId</span></span>
<span data-ttu-id="6649f-126">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6649f-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="6649f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6649f-127">CommonParameters</span></span>
<span data-ttu-id="6649f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6649f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6649f-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6649f-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6649f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6649f-130">INPUTS</span></span>

### <span data-ttu-id="6649f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6649f-131">System.String</span></span>

## <span data-ttu-id="6649f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6649f-132">OUTPUTS</span></span>

### <span data-ttu-id="6649f-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="6649f-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="6649f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6649f-134">NOTES</span></span>

## <span data-ttu-id="6649f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6649f-135">RELATED LINKS</span></span>
