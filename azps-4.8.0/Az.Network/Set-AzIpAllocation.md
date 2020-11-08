---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009044"
---
# <span data-ttu-id="5f7c2-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5f7c2-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="5f7c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f7c2-103">Speichert eine geänderte IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="5f7c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f7c2-104">SYNTAX</span></span>

### <span data-ttu-id="5f7c2-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f7c2-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f7c2-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f7c2-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f7c2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f7c2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f7c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f7c2-108">DESCRIPTION</span></span>
<span data-ttu-id="5f7c2-109">Das Cmdlet " **Satz-AzIpAllocation** " aktualisiert ein Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="5f7c2-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="5f7c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f7c2-110">EXAMPLES</span></span>

### <span data-ttu-id="5f7c2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f7c2-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="5f7c2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f7c2-112">PARAMETERS</span></span>

### <span data-ttu-id="5f7c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f7c2-113">-AsJob</span></span>
<span data-ttu-id="5f7c2-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5f7c2-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f7c2-115">-DefaultProfile</span></span>
<span data-ttu-id="5f7c2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f7c2-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f7c2-117">-InputObject</span></span>
<span data-ttu-id="5f7c2-118">Die IpAllocation</span><span class="sxs-lookup"><span data-stu-id="5f7c2-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="5f7c2-119">-IpAllocationTag</span></span>
<span data-ttu-id="5f7c2-120">Die Zuordnungs Tags der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="5f7c2-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5f7c2-121">-Name</span></span>
<span data-ttu-id="5f7c2-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f7c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f7c2-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f7c2-125">-ResourceId</span></span>
<span data-ttu-id="5f7c2-126">IpAllocation-ID</span><span class="sxs-lookup"><span data-stu-id="5f7c2-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f7c2-127">-Tag</span></span>
<span data-ttu-id="5f7c2-128">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f7c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f7c2-129">CommonParameters</span></span>
<span data-ttu-id="5f7c2-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f7c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f7c2-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f7c2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f7c2-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f7c2-132">INPUTS</span></span>

### <span data-ttu-id="5f7c2-133">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5f7c2-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="5f7c2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f7c2-134">OUTPUTS</span></span>

### <span data-ttu-id="5f7c2-135">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5f7c2-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="5f7c2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f7c2-136">NOTES</span></span>

## <span data-ttu-id="5f7c2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f7c2-137">RELATED LINKS</span></span>
