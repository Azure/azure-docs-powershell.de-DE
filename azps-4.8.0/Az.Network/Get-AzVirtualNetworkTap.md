---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009126"
---
# <span data-ttu-id="f3316-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f3316-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="f3316-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3316-102">SYNOPSIS</span></span>
<span data-ttu-id="f3316-103">Ruft einen virtuellen Netzwerk Hahn ab</span><span class="sxs-lookup"><span data-stu-id="f3316-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="f3316-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3316-104">SYNTAX</span></span>

### <span data-ttu-id="f3316-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3316-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3316-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3316-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3316-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3316-107">DESCRIPTION</span></span>
<span data-ttu-id="f3316-108">Das Cmdlet " **Get-AzVirtualNetworkTap** " Ruft einen virtuellen Azure-Netzwerk Hahn oder eine Liste mit Azure-virtuellen Netzwerk-TAPS in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f3316-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="f3316-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3316-109">EXAMPLES</span></span>

### <span data-ttu-id="f3316-110">Beispiel 1: Abrufen eines virtuellen Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="f3316-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="f3316-111">Dieser Befehl ruft einen VirtualNetwork-Tap-Verweis für den angegebenen "VirtualTap1" in "ResourceGroup1" ab.</span><span class="sxs-lookup"><span data-stu-id="f3316-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="f3316-112">Beispiel 2: Abrufen aller virtuellen Netzwerk-TAPS mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="f3316-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="f3316-113">Dieser Befehl ruft alle VirtualNetwork-Tap-Bezüge ab, die mit "VirtualTap" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f3316-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="f3316-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3316-114">PARAMETERS</span></span>

### <span data-ttu-id="f3316-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3316-115">-DefaultProfile</span></span>
<span data-ttu-id="f3316-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3316-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3316-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f3316-117">-Name</span></span>
<span data-ttu-id="f3316-118">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="f3316-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f3316-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3316-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3316-120">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="f3316-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f3316-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3316-121">-ResourceId</span></span>
<span data-ttu-id="f3316-122">Ressourcenquelle der VirtualNetworkTap-Ressource</span><span class="sxs-lookup"><span data-stu-id="f3316-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3316-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3316-123">-Confirm</span></span>
<span data-ttu-id="f3316-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3316-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3316-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3316-125">-WhatIf</span></span>
<span data-ttu-id="f3316-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3316-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3316-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3316-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3316-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3316-128">CommonParameters</span></span>
<span data-ttu-id="f3316-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3316-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3316-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3316-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3316-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3316-131">INPUTS</span></span>

### <span data-ttu-id="f3316-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f3316-132">System.String</span></span>

## <span data-ttu-id="f3316-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3316-133">OUTPUTS</span></span>

### <span data-ttu-id="f3316-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f3316-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="f3316-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3316-135">NOTES</span></span>

## <span data-ttu-id="f3316-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3316-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3316-137">Neu – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f3316-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="f3316-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f3316-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="f3316-139">Satz-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f3316-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
