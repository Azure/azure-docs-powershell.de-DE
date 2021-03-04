---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920531"
---
# <span data-ttu-id="2590e-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="2590e-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="2590e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2590e-102">SYNOPSIS</span></span>
<span data-ttu-id="2590e-103">Legen Sie das übergeordnete Gerät des angegebenen Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="2590e-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="2590e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2590e-104">SYNTAX</span></span>

### <span data-ttu-id="2590e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2590e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2590e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2590e-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2590e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2590e-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2590e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2590e-108">DESCRIPTION</span></span>
<span data-ttu-id="2590e-109">Legen Sie das übergeordnete Gerät des angegebenen Nicht-Edge-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="2590e-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="2590e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2590e-110">EXAMPLES</span></span>

### <span data-ttu-id="2590e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2590e-111">Example 1</span></span>
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

## <span data-ttu-id="2590e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2590e-112">PARAMETERS</span></span>

### <span data-ttu-id="2590e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2590e-113">-DefaultProfile</span></span>
<span data-ttu-id="2590e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2590e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2590e-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2590e-115">-DeviceId</span></span>
<span data-ttu-id="2590e-116">ID eines Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="2590e-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="2590e-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2590e-117">-Force</span></span>
<span data-ttu-id="2590e-118">Überschreibt das übergeordnete Gerät des Nicht-Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="2590e-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="2590e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2590e-119">-InputObject</span></span>
<span data-ttu-id="2590e-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="2590e-120">IotHub object</span></span>

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

### <span data-ttu-id="2590e-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2590e-121">-IotHubName</span></span>
<span data-ttu-id="2590e-122">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="2590e-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2590e-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="2590e-123">-ParentDeviceId</span></span>
<span data-ttu-id="2590e-124">ID des Edgegeräts.</span><span class="sxs-lookup"><span data-stu-id="2590e-124">Id of edge device.</span></span>

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

### <span data-ttu-id="2590e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2590e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2590e-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2590e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2590e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2590e-127">-ResourceId</span></span>
<span data-ttu-id="2590e-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2590e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2590e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2590e-129">-Confirm</span></span>
<span data-ttu-id="2590e-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2590e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2590e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2590e-131">-WhatIf</span></span>
<span data-ttu-id="2590e-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2590e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2590e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2590e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2590e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2590e-134">CommonParameters</span></span>
<span data-ttu-id="2590e-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2590e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2590e-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2590e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2590e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2590e-137">INPUTS</span></span>

### <span data-ttu-id="2590e-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2590e-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2590e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2590e-139">System.String</span></span>

## <span data-ttu-id="2590e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2590e-140">OUTPUTS</span></span>

### <span data-ttu-id="2590e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="2590e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="2590e-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2590e-142">NOTES</span></span>

## <span data-ttu-id="2590e-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2590e-143">RELATED LINKS</span></span>
