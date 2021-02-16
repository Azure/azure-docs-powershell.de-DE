---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154881"
---
# <span data-ttu-id="263a1-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="263a1-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="263a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="263a1-102">SYNOPSIS</span></span>
<span data-ttu-id="263a1-103">Erstellt eine neue IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="263a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="263a1-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="263a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="263a1-105">DESCRIPTION</span></span>
<span data-ttu-id="263a1-106">Erstellt eine neue IoT-Zentralanwendung mit den bereitgestellten Eigenschaften und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="263a1-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="263a1-107">Eine Einführung in IoT Central finden Sie unter https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="263a1-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="263a1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="263a1-108">EXAMPLES</span></span>

### <span data-ttu-id="263a1-109">Beispiel 1: Erstellen einer einfachen zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="263a1-110">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="263a1-110">Example Output:</span></span>

<span data-ttu-id="263a1-111">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location: westus Tag : SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263a1-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="263a1-112">Erstellen Sie eine IoT Central-Anwendung in der Standardpreisebene ST2 in der Region der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="263a1-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="263a1-113">Beispiel 2 Erstellen einer einfachen zentralen IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="263a1-114">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="263a1-114">Example Output:</span></span>

<span data-ttu-id="263a1-115">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location: westus Tag : SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Meine Benutzerdefinierte Unterdomäne für Anzeigenamen: MeineAppSubdomain-Vorlage: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263a1-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="263a1-116">Erstellen Sie eine IoT Central-Anwendung mit der Standardpreisstufe ST2 in der Region "westus" mit einem benutzerdefinierten Anzeigenamen, basierend auf der iotc-default-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="263a1-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="263a1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="263a1-117">PARAMETERS</span></span>

### <span data-ttu-id="263a1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="263a1-118">-AsJob</span></span>
<span data-ttu-id="263a1-119">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="263a1-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="263a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263a1-120">-DefaultProfile</span></span>
<span data-ttu-id="263a1-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="263a1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263a1-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="263a1-122">-DisplayName</span></span>
<span data-ttu-id="263a1-123">Benutzerdefinierter Anzeigename für die IoT Central-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="263a1-124">Der Standard ist der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="263a1-124">Default is resource name.</span></span>

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

### <span data-ttu-id="263a1-125">-Location</span><span class="sxs-lookup"><span data-stu-id="263a1-125">-Location</span></span>
<span data-ttu-id="263a1-126">Speicherort Ihrer IoT Central-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="263a1-127">Der Standard ist der Speicherort der Zielressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="263a1-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="263a1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="263a1-128">-Name</span></span>
<span data-ttu-id="263a1-129">Name der zentralen Anwendungsressource "Iot".</span><span class="sxs-lookup"><span data-stu-id="263a1-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="263a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="263a1-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="263a1-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263a1-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="263a1-132">-Sku</span></span>
<span data-ttu-id="263a1-133">Preisstufe für IoT Central-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="263a1-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="263a1-134">Der Standardwert ist ST2.</span><span class="sxs-lookup"><span data-stu-id="263a1-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="263a1-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="263a1-135">-Subdomain</span></span>
<span data-ttu-id="263a1-136">Unterdomäne für die IoT Central-URL.</span><span class="sxs-lookup"><span data-stu-id="263a1-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="263a1-137">Jede Anwendung muss über eine eindeutige Unterdomäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="263a1-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263a1-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="263a1-138">-Tag</span></span>
<span data-ttu-id="263a1-139">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="263a1-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="263a1-140">-Template</span><span class="sxs-lookup"><span data-stu-id="263a1-140">-Template</span></span>
<span data-ttu-id="263a1-141">Name der IoT Central-Anwendungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="263a1-141">IoT Central application template name.</span></span>
<span data-ttu-id="263a1-142">Standard ist eine benutzerdefinierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="263a1-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="263a1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="263a1-143">-Confirm</span></span>
<span data-ttu-id="263a1-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="263a1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="263a1-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="263a1-145">-WhatIf</span></span>
<span data-ttu-id="263a1-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="263a1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263a1-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="263a1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="263a1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263a1-148">CommonParameters</span></span>
<span data-ttu-id="263a1-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263a1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263a1-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="263a1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263a1-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="263a1-151">INPUTS</span></span>

### <span data-ttu-id="263a1-152">System.String</span><span class="sxs-lookup"><span data-stu-id="263a1-152">System.String</span></span>

### <span data-ttu-id="263a1-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="263a1-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="263a1-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="263a1-154">OUTPUTS</span></span>

### <span data-ttu-id="263a1-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="263a1-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="263a1-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="263a1-156">NOTES</span></span>

## <span data-ttu-id="263a1-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="263a1-157">RELATED LINKS</span></span>
