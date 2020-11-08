---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174515"
---
# <span data-ttu-id="0a321-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0a321-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="0a321-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a321-102">SYNOPSIS</span></span>
<span data-ttu-id="0a321-103">Ändern oder Ändern einer virtuellen Appliance-Website, die mit einer virtuellen Netzwerk-Appliance-Ressource verbunden ist</span><span class="sxs-lookup"><span data-stu-id="0a321-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0a321-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a321-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a321-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a321-105">DESCRIPTION</span></span>
<span data-ttu-id="0a321-106">Mit dem Befehl Update-AzVirtualApplianceSite wird eine Website Ressource einer virtuellen Appliance geändert.</span><span class="sxs-lookup"><span data-stu-id="0a321-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="0a321-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a321-107">EXAMPLES</span></span>

### <span data-ttu-id="0a321-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a321-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="0a321-109">Ändern Sie das Adresspräfix für eine Website Ressource einer virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="0a321-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="0a321-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a321-110">PARAMETERS</span></span>

### <span data-ttu-id="0a321-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="0a321-111">-AddresssPrefix</span></span>
<span data-ttu-id="0a321-112">Das Adresspräfix für die Website.</span><span class="sxs-lookup"><span data-stu-id="0a321-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a321-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a321-113">-AsJob</span></span>
<span data-ttu-id="0a321-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a321-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a321-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a321-115">-DefaultProfile</span></span>
<span data-ttu-id="0a321-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a321-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a321-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0a321-117">-Force</span></span>
<span data-ttu-id="0a321-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="0a321-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0a321-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0a321-119">-Name</span></span>
<span data-ttu-id="0a321-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0a321-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a321-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="0a321-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="0a321-122">Virtuelle Netzwerk-Appliance, an die diese Website angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="0a321-122">Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a321-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="0a321-123">-O365Policy</span></span>
<span data-ttu-id="0a321-124">Office 365-Breakout-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0a321-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a321-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a321-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a321-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a321-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a321-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a321-127">-Tag</span></span>
<span data-ttu-id="0a321-128">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a321-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0a321-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a321-129">-Confirm</span></span>
<span data-ttu-id="0a321-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a321-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a321-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a321-131">-WhatIf</span></span>
<span data-ttu-id="0a321-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a321-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a321-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a321-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a321-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a321-134">CommonParameters</span></span>
<span data-ttu-id="0a321-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a321-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a321-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a321-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a321-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a321-137">INPUTS</span></span>

### <span data-ttu-id="0a321-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0a321-138">System.String</span></span>

### <span data-ttu-id="0a321-139">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="0a321-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="0a321-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a321-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a321-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a321-141">OUTPUTS</span></span>

### <span data-ttu-id="0a321-142">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0a321-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="0a321-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a321-143">NOTES</span></span>

## <span data-ttu-id="0a321-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a321-144">RELATED LINKS</span></span>
