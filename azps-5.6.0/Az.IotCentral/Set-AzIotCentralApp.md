---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942568"
---
# <span data-ttu-id="c081c-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="c081c-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="c081c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c081c-102">SYNOPSIS</span></span>
<span data-ttu-id="c081c-103">Aktualisiert die Metadaten für eine zentrale IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="c081c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c081c-104">SYNTAX</span></span>

### <span data-ttu-id="c081c-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c081c-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c081c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c081c-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c081c-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="c081c-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c081c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c081c-108">DESCRIPTION</span></span>
<span data-ttu-id="c081c-109">Aktualisieren Sie die Metadaten für eine zentrale IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="c081c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c081c-110">EXAMPLES</span></span>

### <span data-ttu-id="c081c-111">Beispiel 1 Anzeigename aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c081c-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="c081c-112">Aktualisieren Sie den Anzeigenamen in einer vorhandenen Zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="c081c-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="c081c-113">Example Output:</span></span>

<span data-ttu-id="c081c-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My New Custom Display Name Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c081c-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="c081c-115">Beispiel 2 Unterdomäne aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c081c-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="c081c-116">Aktualisieren Sie den Anzeigenamen in einer vorhandenen Zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="c081c-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="c081c-117">Example Output:</span></span>

<span data-ttu-id="c081c-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp ApplicationId von SkuInfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Display Name Subdomain : new-subdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c081c-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="c081c-119">Beispiel 3 Aktualisieren von App-Sku-Informationen</span><span class="sxs-lookup"><span data-stu-id="c081c-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="c081c-120">Aktualisieren Sie die Sku für eine vorhandene Zentrale IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="c081c-121">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="c081c-121">Example Output:</span></span>

<span data-ttu-id="c081c-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp ApplicationId von SkuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Display Name Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c081c-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="c081c-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c081c-123">PARAMETERS</span></span>

### <span data-ttu-id="c081c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c081c-124">-AsJob</span></span>
<span data-ttu-id="c081c-125">Führen Sie das Cmdlet als Auftrag im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="c081c-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="c081c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c081c-126">-DefaultProfile</span></span>
<span data-ttu-id="c081c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c081c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c081c-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c081c-128">-DisplayName</span></span>
<span data-ttu-id="c081c-129">Benutzerdefinierter Anzeigename der zentralen Iot-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="c081c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c081c-130">-InputObject</span></span>
<span data-ttu-id="c081c-131">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="c081c-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c081c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c081c-132">-Name</span></span>
<span data-ttu-id="c081c-133">Name der zentralen Anwendungsressource Iot.</span><span class="sxs-lookup"><span data-stu-id="c081c-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c081c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c081c-134">-ResourceGroupName</span></span>
<span data-ttu-id="c081c-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c081c-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c081c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c081c-136">-ResourceId</span></span>
<span data-ttu-id="c081c-137">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="c081c-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c081c-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="c081c-138">-Sku</span></span>
<span data-ttu-id="c081c-139">Preisstufen für IoT Central-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c081c-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="c081c-140">Der Standardwert ist ST2.</span><span class="sxs-lookup"><span data-stu-id="c081c-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="c081c-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="c081c-141">-Subdomain</span></span>
<span data-ttu-id="c081c-142">Unterdomäne der zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c081c-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="c081c-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c081c-143">-Tag</span></span>
<span data-ttu-id="c081c-144">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="c081c-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c081c-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c081c-145">-Confirm</span></span>
<span data-ttu-id="c081c-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c081c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c081c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c081c-147">-WhatIf</span></span>
<span data-ttu-id="c081c-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c081c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c081c-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c081c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c081c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c081c-150">CommonParameters</span></span>
<span data-ttu-id="c081c-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c081c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c081c-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c081c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c081c-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c081c-153">INPUTS</span></span>

### <span data-ttu-id="c081c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c081c-154">System.String</span></span>

### <span data-ttu-id="c081c-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="c081c-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="c081c-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c081c-156">OUTPUTS</span></span>

### <span data-ttu-id="c081c-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="c081c-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="c081c-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c081c-158">NOTES</span></span>

## <span data-ttu-id="c081c-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c081c-159">RELATED LINKS</span></span>
