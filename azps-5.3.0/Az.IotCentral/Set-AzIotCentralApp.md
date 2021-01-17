---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472510"
---
# <span data-ttu-id="d6a86-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d6a86-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="d6a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a86-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a86-103">Aktualisiert die Metadaten für eine IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="d6a86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6a86-104">SYNTAX</span></span>

### <span data-ttu-id="d6a86-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6a86-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a86-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a86-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a86-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a86-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6a86-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6a86-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a86-109">Aktualisieren Sie die Metadaten für eine IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="d6a86-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6a86-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a86-111">Beispiel 1 Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="d6a86-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="d6a86-112">Aktualisieren Sie den Anzeigenamen für eine vorhandene IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="d6a86-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="d6a86-113">Example Output:</span></span>

<span data-ttu-id="d6a86-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location: westus Tag : SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="d6a86-115">Beispiel 2 Aktualisieren einer Subdomäne</span><span class="sxs-lookup"><span data-stu-id="d6a86-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="d6a86-116">Aktualisieren Sie den Anzeigenamen für eine vorhandene IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="d6a86-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="d6a86-117">Example Output:</span></span>

<span data-ttu-id="d6a86-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp Anwendungs-ID derKuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Display Name Subdomain : new-subdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="d6a86-119">Beispiel 3 Aktualisieren der Infos zur App-SKU</span><span class="sxs-lookup"><span data-stu-id="d6a86-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="d6a86-120">Aktualisieren Sie die SKU für eine vorhandene IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="d6a86-121">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="d6a86-121">Example Output:</span></span>

<span data-ttu-id="d6a86-122">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp Anwendungs-Id: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Unterdomäne "Anzeigename": Vorlage "MyAppSubdomain": iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="d6a86-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6a86-123">PARAMETERS</span></span>

### <span data-ttu-id="d6a86-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6a86-124">-AsJob</span></span>
<span data-ttu-id="d6a86-125">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="d6a86-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d6a86-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a86-126">-DefaultProfile</span></span>
<span data-ttu-id="d6a86-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6a86-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a86-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6a86-128">-DisplayName</span></span>
<span data-ttu-id="d6a86-129">Benutzerdefinierter Anzeigename der zentralen Anwendung "Iot".</span><span class="sxs-lookup"><span data-stu-id="d6a86-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="d6a86-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6a86-130">-InputObject</span></span>
<span data-ttu-id="d6a86-131">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="d6a86-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="d6a86-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d6a86-132">-Name</span></span>
<span data-ttu-id="d6a86-133">Name der zentralen Anwendungsressource "Iot".</span><span class="sxs-lookup"><span data-stu-id="d6a86-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d6a86-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-134">-ResourceGroupName</span></span>
<span data-ttu-id="d6a86-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6a86-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d6a86-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a86-136">-ResourceId</span></span>
<span data-ttu-id="d6a86-137">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="d6a86-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="d6a86-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d6a86-138">-Sku</span></span>
<span data-ttu-id="d6a86-139">Preisstufe für IoT Central-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d6a86-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="d6a86-140">Der Standardwert ist ST2.</span><span class="sxs-lookup"><span data-stu-id="d6a86-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="d6a86-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="d6a86-141">-Subdomain</span></span>
<span data-ttu-id="d6a86-142">Unterdomäne der zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d6a86-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="d6a86-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6a86-143">-Tag</span></span>
<span data-ttu-id="d6a86-144">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="d6a86-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="d6a86-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6a86-145">-Confirm</span></span>
<span data-ttu-id="d6a86-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6a86-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a86-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d6a86-147">-WhatIf</span></span>
<span data-ttu-id="d6a86-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6a86-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a86-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6a86-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a86-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a86-150">CommonParameters</span></span>
<span data-ttu-id="d6a86-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a86-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a86-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6a86-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a86-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6a86-153">INPUTS</span></span>

### <span data-ttu-id="d6a86-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d6a86-154">System.String</span></span>

### <span data-ttu-id="d6a86-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d6a86-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d6a86-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6a86-156">OUTPUTS</span></span>

### <span data-ttu-id="d6a86-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d6a86-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d6a86-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d6a86-158">NOTES</span></span>

## <span data-ttu-id="d6a86-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d6a86-159">RELATED LINKS</span></span>
