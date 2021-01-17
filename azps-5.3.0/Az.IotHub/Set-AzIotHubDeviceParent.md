---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386544"
---
# <span data-ttu-id="284d6-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="284d6-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="284d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="284d6-102">SYNOPSIS</span></span>
<span data-ttu-id="284d6-103">Legen Sie das übergeordnete Gerät des angegebenen Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="284d6-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="284d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="284d6-104">SYNTAX</span></span>

### <span data-ttu-id="284d6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="284d6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="284d6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="284d6-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="284d6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="284d6-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="284d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="284d6-108">DESCRIPTION</span></span>
<span data-ttu-id="284d6-109">Legen Sie das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="284d6-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="284d6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="284d6-110">EXAMPLES</span></span>

### <span data-ttu-id="284d6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="284d6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="284d6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="284d6-112">PARAMETERS</span></span>

### <span data-ttu-id="284d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284d6-113">-DefaultProfile</span></span>
<span data-ttu-id="284d6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="284d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="284d6-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="284d6-115">-DeviceId</span></span>
<span data-ttu-id="284d6-116">ID eines Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="284d6-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="284d6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="284d6-117">-Force</span></span>
<span data-ttu-id="284d6-118">Überschreibt das übergeordnete Gerät des Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="284d6-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="284d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="284d6-119">-InputObject</span></span>
<span data-ttu-id="284d6-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="284d6-120">IotHub object</span></span>

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

### <span data-ttu-id="284d6-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="284d6-121">-IotHubName</span></span>
<span data-ttu-id="284d6-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="284d6-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="284d6-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="284d6-123">-ParentDeviceId</span></span>
<span data-ttu-id="284d6-124">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="284d6-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="284d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="284d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="284d6-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="284d6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="284d6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="284d6-127">-ResourceId</span></span>
<span data-ttu-id="284d6-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="284d6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="284d6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="284d6-129">-Confirm</span></span>
<span data-ttu-id="284d6-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="284d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="284d6-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="284d6-131">-WhatIf</span></span>
<span data-ttu-id="284d6-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="284d6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="284d6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="284d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="284d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284d6-134">CommonParameters</span></span>
<span data-ttu-id="284d6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="284d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284d6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="284d6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284d6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="284d6-137">INPUTS</span></span>

### <span data-ttu-id="284d6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="284d6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="284d6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="284d6-139">System.String</span></span>

## <span data-ttu-id="284d6-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="284d6-140">OUTPUTS</span></span>

### <span data-ttu-id="284d6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEntfernung</span><span class="sxs-lookup"><span data-stu-id="284d6-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="284d6-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="284d6-142">NOTES</span></span>

## <span data-ttu-id="284d6-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="284d6-143">RELATED LINKS</span></span>
