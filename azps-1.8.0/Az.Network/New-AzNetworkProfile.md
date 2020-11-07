---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660513"
---
# <span data-ttu-id="61f04-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="61f04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61f04-102">SYNOPSIS</span></span>
<span data-ttu-id="61f04-103">Erstellt ein neues Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="61f04-103">Creates a new network profile.</span></span>

## <span data-ttu-id="61f04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61f04-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f04-105">DESCRIPTION</span></span>
<span data-ttu-id="61f04-106">Das Cmdlet **New-AzNetworkProfile** erstellt eine neue Ressource für das Netzwerkprofil auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="61f04-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="61f04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61f04-107">EXAMPLES</span></span>

### <span data-ttu-id="61f04-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61f04-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="61f04-109">Dadurch wird eine neue Ressource für das Netzwerkprofil auf oberster Ebene erstellt</span><span class="sxs-lookup"><span data-stu-id="61f04-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="61f04-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61f04-110">PARAMETERS</span></span>

### <span data-ttu-id="61f04-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61f04-111">-AsJob</span></span>
<span data-ttu-id="61f04-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61f04-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61f04-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="61f04-113">-ContainerNicConfig</span></span>
<span data-ttu-id="61f04-114">Die Container-Netzwerkschnittstellen Konfigurationen, die diesem Netzwerkprofil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61f04-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="61f04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-115">-DefaultProfile</span></span>
<span data-ttu-id="61f04-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61f04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f04-117">-Force</span><span class="sxs-lookup"><span data-stu-id="61f04-117">-Force</span></span>
<span data-ttu-id="61f04-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="61f04-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="61f04-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="61f04-119">-Location</span></span>
<span data-ttu-id="61f04-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="61f04-120">The location.</span></span>

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

### <span data-ttu-id="61f04-121">-Name</span><span class="sxs-lookup"><span data-stu-id="61f04-121">-Name</span></span>
<span data-ttu-id="61f04-122">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="61f04-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="61f04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f04-123">-ResourceGroupName</span></span>
<span data-ttu-id="61f04-124">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="61f04-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="61f04-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="61f04-125">-Tag</span></span>
<span data-ttu-id="61f04-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="61f04-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="61f04-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61f04-127">-Confirm</span></span>
<span data-ttu-id="61f04-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f04-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f04-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f04-129">-WhatIf</span></span>
<span data-ttu-id="61f04-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f04-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f04-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f04-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f04-132">CommonParameters</span></span>
<span data-ttu-id="61f04-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f04-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f04-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f04-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61f04-135">INPUTS</span></span>

### <span data-ttu-id="61f04-136">System. String</span><span class="sxs-lookup"><span data-stu-id="61f04-136">System.String</span></span>

### <span data-ttu-id="61f04-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="61f04-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="61f04-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="61f04-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="61f04-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61f04-139">OUTPUTS</span></span>

### <span data-ttu-id="61f04-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="61f04-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="61f04-141">NOTES</span></span>

## <span data-ttu-id="61f04-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61f04-142">RELATED LINKS</span></span>

[<span data-ttu-id="61f04-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="61f04-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="61f04-145">Satz-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61f04-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
