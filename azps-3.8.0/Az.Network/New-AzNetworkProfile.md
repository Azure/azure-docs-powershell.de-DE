---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996764"
---
# <span data-ttu-id="b1d1a-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="b1d1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d1a-103">Erstellt ein neues Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-103">Creates a new network profile.</span></span>

## <span data-ttu-id="b1d1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d1a-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1d1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d1a-106">Das Cmdlet **New-AzNetworkProfile** erstellt eine neue Ressource für das Netzwerkprofil auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="b1d1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1d1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d1a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1d1a-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="b1d1a-109">Dadurch wird eine neue Ressource für das Netzwerkprofil auf oberster Ebene erstellt</span><span class="sxs-lookup"><span data-stu-id="b1d1a-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="b1d1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1d1a-110">PARAMETERS</span></span>

### <span data-ttu-id="b1d1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1d1a-111">-AsJob</span></span>
<span data-ttu-id="b1d1a-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1d1a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1d1a-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b1d1a-113">-ContainerNicConfig</span></span>
<span data-ttu-id="b1d1a-114">Die Container-Netzwerkschnittstellen Konfigurationen, die diesem Netzwerkprofil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-115">-DefaultProfile</span></span>
<span data-ttu-id="b1d1a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d1a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b1d1a-117">-Force</span></span>
<span data-ttu-id="b1d1a-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="b1d1a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b1d1a-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="b1d1a-119">-Location</span></span>
<span data-ttu-id="b1d1a-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-120">The location.</span></span>

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

### <span data-ttu-id="b1d1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1d1a-121">-Name</span></span>
<span data-ttu-id="b1d1a-122">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="b1d1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1d1a-124">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="b1d1a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1d1a-125">-Tag</span></span>
<span data-ttu-id="b1d1a-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b1d1a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1d1a-127">-Confirm</span></span>
<span data-ttu-id="b1d1a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1d1a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d1a-129">-WhatIf</span></span>
<span data-ttu-id="b1d1a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d1a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1d1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d1a-132">CommonParameters</span></span>
<span data-ttu-id="b1d1a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d1a-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d1a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d1a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1d1a-135">INPUTS</span></span>

### <span data-ttu-id="b1d1a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d1a-136">System.String</span></span>

### <span data-ttu-id="b1d1a-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b1d1a-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b1d1a-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b1d1a-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="b1d1a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1d1a-139">OUTPUTS</span></span>

### <span data-ttu-id="b1d1a-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b1d1a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1d1a-141">NOTES</span></span>

## <span data-ttu-id="b1d1a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1d1a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1d1a-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="b1d1a-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="b1d1a-145">Satz-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
