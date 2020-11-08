---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004546"
---
# <span data-ttu-id="e5a4b-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e5a4b-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="e5a4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a4b-103">Hinzufügen von nicht-Edge-Geräten als untergeordnete Geräte zum Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="e5a4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a4b-104">SYNTAX</span></span>

### <span data-ttu-id="e5a4b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5a4b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5a4b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5a4b-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5a4b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5a4b-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a4b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="e5a4b-109">Fügen Sie die angegebene durch Kommas getrennte Liste der nicht-Edge-Geräte-IDs als untergeordnete Elemente des angegebenen Edge-Geräts hinzu.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="e5a4b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a4b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5a4b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="e5a4b-112">Hinzufügen von nicht-Edge-Geräten als untergeordnete Geräte zum Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="e5a4b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5a4b-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="e5a4b-114">Hinzufügen von nicht-Edge-Geräten als untergeordnete Elemente zum Edge-Gerät unabhängig davon ist das nicht-Edge-Gerät bereits ein untergeordnetes Element eines anderen Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="e5a4b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a4b-115">PARAMETERS</span></span>

### <span data-ttu-id="e5a4b-116">-Kinder</span><span class="sxs-lookup"><span data-stu-id="e5a4b-116">-Children</span></span>
<span data-ttu-id="e5a4b-117">Liste der untergeordneten Geräte (durch Kommas getrennt) enthält nur nicht-Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a4b-118">-DefaultProfile</span></span>
<span data-ttu-id="e5a4b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a4b-120">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="e5a4b-120">-DeviceId</span></span>
<span data-ttu-id="e5a4b-121">Die ID des Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e5a4b-122">-Force</span></span>
<span data-ttu-id="e5a4b-123">Überschreibt das übergeordnete Gerät des nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="e5a4b-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5a4b-124">-InputObject</span></span>
<span data-ttu-id="e5a4b-125">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="e5a4b-125">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e5a4b-126">-IotHubName</span></span>
<span data-ttu-id="e5a4b-127">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="e5a4b-127">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a4b-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5a4b-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e5a4b-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e5a4b-130">-ResourceId</span></span>
<span data-ttu-id="e5a4b-131">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e5a4b-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a4b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5a4b-132">-Confirm</span></span>
<span data-ttu-id="e5a4b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a4b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a4b-134">-WhatIf</span></span>
<span data-ttu-id="e5a4b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a4b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a4b-137">CommonParameters</span></span>
<span data-ttu-id="e5a4b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a4b-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a4b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a4b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5a4b-140">INPUTS</span></span>

### <span data-ttu-id="e5a4b-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5a4b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5a4b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a4b-142">System.String</span></span>

## <span data-ttu-id="e5a4b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5a4b-143">OUTPUTS</span></span>

### <span data-ttu-id="e5a4b-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e5a4b-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="e5a4b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5a4b-145">NOTES</span></span>

## <span data-ttu-id="e5a4b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5a4b-146">RELATED LINKS</span></span>
