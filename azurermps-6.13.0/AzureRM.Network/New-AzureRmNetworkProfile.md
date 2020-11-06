---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495889"
---
# <span data-ttu-id="77f37-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="77f37-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="77f37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77f37-102">SYNOPSIS</span></span>
<span data-ttu-id="77f37-103">Erstellt ein neues Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="77f37-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77f37-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77f37-105">DESCRIPTION</span></span>
<span data-ttu-id="77f37-106">Das Cmdlet **New-AzureRmNetworkProfile** erstellt eine neue Ressource für das Netzwerkprofil auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="77f37-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="77f37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77f37-107">EXAMPLES</span></span>

### <span data-ttu-id="77f37-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77f37-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="77f37-109">Dadurch wird eine neue Ressource für das Netzwerkprofil auf oberster Ebene erstellt</span><span class="sxs-lookup"><span data-stu-id="77f37-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="77f37-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="77f37-110">PARAMETERS</span></span>

### <span data-ttu-id="77f37-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f37-111">-AsJob</span></span>
<span data-ttu-id="77f37-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="77f37-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f37-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="77f37-113">-ContainerNicConfig</span></span>
<span data-ttu-id="77f37-114">Die Container-Netzwerkschnittstellen Konfigurationen, die diesem Netzwerkprofil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77f37-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="77f37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f37-115">-DefaultProfile</span></span>
<span data-ttu-id="77f37-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77f37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f37-117">-Force</span><span class="sxs-lookup"><span data-stu-id="77f37-117">-Force</span></span>
<span data-ttu-id="77f37-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="77f37-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="77f37-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="77f37-119">-Location</span></span>
<span data-ttu-id="77f37-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="77f37-120">The location.</span></span>

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

### <span data-ttu-id="77f37-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77f37-121">-Name</span></span>
<span data-ttu-id="77f37-122">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="77f37-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="77f37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f37-123">-ResourceGroupName</span></span>
<span data-ttu-id="77f37-124">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="77f37-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="77f37-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="77f37-125">-Tag</span></span>
<span data-ttu-id="77f37-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="77f37-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="77f37-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77f37-127">-Confirm</span></span>
<span data-ttu-id="77f37-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77f37-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f37-129">-WhatIf</span></span>
<span data-ttu-id="77f37-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77f37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f37-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77f37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f37-132">CommonParameters</span></span>
<span data-ttu-id="77f37-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f37-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f37-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f37-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77f37-135">INPUTS</span></span>

### <span data-ttu-id="77f37-136">System. String</span><span class="sxs-lookup"><span data-stu-id="77f37-136">System.String</span></span>

### <span data-ttu-id="77f37-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="77f37-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="77f37-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterface, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77f37-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="77f37-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77f37-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="77f37-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77f37-140">OUTPUTS</span></span>

### <span data-ttu-id="77f37-141">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="77f37-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="77f37-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="77f37-142">NOTES</span></span>

## <span data-ttu-id="77f37-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77f37-143">RELATED LINKS</span></span>
