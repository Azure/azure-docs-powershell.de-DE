---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996213"
---
# <span data-ttu-id="f5eaf-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f5eaf-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="f5eaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="f5eaf-103">Löschen von Modulen auf einem Ziel-viel-Gerät in einem viel Hub</span><span class="sxs-lookup"><span data-stu-id="f5eaf-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f5eaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5eaf-104">SYNTAX</span></span>

### <span data-ttu-id="f5eaf-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5eaf-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5eaf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5eaf-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5eaf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5eaf-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5eaf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5eaf-108">DESCRIPTION</span></span>
<span data-ttu-id="f5eaf-109">Löschen von Modulen auf einem Ziel-viel-Gerät in einem viel Hub</span><span class="sxs-lookup"><span data-stu-id="f5eaf-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f5eaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5eaf-110">EXAMPLES</span></span>

### <span data-ttu-id="f5eaf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5eaf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="f5eaf-112">Löschen eines viel Geräte Moduls</span><span class="sxs-lookup"><span data-stu-id="f5eaf-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="f5eaf-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f5eaf-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="f5eaf-114">Löschen Sie alle Gerätemodule.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="f5eaf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5eaf-115">PARAMETERS</span></span>

### <span data-ttu-id="f5eaf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5eaf-116">-DefaultProfile</span></span>
<span data-ttu-id="f5eaf-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5eaf-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="f5eaf-118">-DeviceId</span></span>
<span data-ttu-id="f5eaf-119">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-119">Target Device Id.</span></span>

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

### <span data-ttu-id="f5eaf-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5eaf-120">-InputObject</span></span>
<span data-ttu-id="f5eaf-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f5eaf-121">IotHub object</span></span>

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

### <span data-ttu-id="f5eaf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f5eaf-122">-IotHubName</span></span>
<span data-ttu-id="f5eaf-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="f5eaf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f5eaf-124">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="f5eaf-124">-ModuleId</span></span>
<span data-ttu-id="f5eaf-125">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5eaf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5eaf-126">-PassThru</span></span>
<span data-ttu-id="f5eaf-127">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="f5eaf-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5eaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5eaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5eaf-130">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f5eaf-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f5eaf-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f5eaf-131">-ResourceId</span></span>
<span data-ttu-id="f5eaf-132">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f5eaf-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f5eaf-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5eaf-133">-Confirm</span></span>
<span data-ttu-id="f5eaf-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5eaf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5eaf-135">-WhatIf</span></span>
<span data-ttu-id="f5eaf-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5eaf-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5eaf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5eaf-138">CommonParameters</span></span>
<span data-ttu-id="f5eaf-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5eaf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5eaf-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5eaf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5eaf-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5eaf-141">INPUTS</span></span>

### <span data-ttu-id="f5eaf-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f5eaf-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f5eaf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f5eaf-143">System.String</span></span>

## <span data-ttu-id="f5eaf-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5eaf-144">OUTPUTS</span></span>

### <span data-ttu-id="f5eaf-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5eaf-145">System.Boolean</span></span>

## <span data-ttu-id="f5eaf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5eaf-146">NOTES</span></span>

## <span data-ttu-id="f5eaf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5eaf-147">RELATED LINKS</span></span>
