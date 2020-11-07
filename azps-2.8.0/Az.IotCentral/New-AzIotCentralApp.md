---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651007"
---
# <span data-ttu-id="e02d0-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e02d0-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="e02d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e02d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e02d0-103">Erstellt eine neue viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="e02d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e02d0-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e02d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e02d0-106">Erstellt eine neue viel zentrale Anwendung mit den bereitgestellten Eigenschaften und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="e02d0-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="e02d0-107">Eine Einführung in "viel Central" finden Sie unter https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="e02d0-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="e02d0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e02d0-108">EXAMPLES</span></span>

### <span data-ttu-id="e02d0-109">Beispiel 1 Erstellen einer einfachen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="e02d0-110">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="e02d0-110">Example Output:</span></span>

<span data-ttu-id="e02d0-111">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: MyAppResourceName Subdomain: MyAppSubdomain-Vorlage: Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx iotc-default@1.0.0 ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02d0-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e02d0-112">Erstellen Sie im Bereich der Ressourcengruppe eine sehr zentrale Anwendung in der Standardpreis Stufe S1.</span><span class="sxs-lookup"><span data-stu-id="e02d0-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="e02d0-113">Beispiel 2 Erstellen einer einfachen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="e02d0-114">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="e02d0-114">Example Output:</span></span>

<span data-ttu-id="e02d0-115">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName-benutzerdefinierte Anzeige Name-Unterdomäne: MyAppSubdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02d0-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e02d0-116">Erstellen Sie eine sehr zentrale Anwendung mit der standardmäßigen Preisstufe S1 in der Region "westus" mit einem benutzerdefinierten Anzeige Namen, der auf der IOTC-Standardvorlage basiert.</span><span class="sxs-lookup"><span data-stu-id="e02d0-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="e02d0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e02d0-117">PARAMETERS</span></span>

### <span data-ttu-id="e02d0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e02d0-118">-AsJob</span></span>
<span data-ttu-id="e02d0-119">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="e02d0-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="e02d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02d0-120">-DefaultProfile</span></span>
<span data-ttu-id="e02d0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e02d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02d0-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e02d0-122">-DisplayName</span></span>
<span data-ttu-id="e02d0-123">Benutzerdefinierter Anzeigename für die viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="e02d0-124">Standard ist der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e02d0-124">Default is resource name.</span></span>

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

### <span data-ttu-id="e02d0-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="e02d0-125">-Location</span></span>
<span data-ttu-id="e02d0-126">Die Position Ihrer zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="e02d0-127">Standard ist der Speicherort der Ziel Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e02d0-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="e02d0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e02d0-128">-Name</span></span>
<span data-ttu-id="e02d0-129">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="e02d0-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="e02d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="e02d0-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e02d0-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e02d0-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="e02d0-132">-Sku</span></span>
<span data-ttu-id="e02d0-133">Preisstufe für viele zentrale Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e02d0-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="e02d0-134">Der Standardwert ist S1.</span><span class="sxs-lookup"><span data-stu-id="e02d0-134">Default value is S1.</span></span>

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

### <span data-ttu-id="e02d0-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="e02d0-135">-Subdomain</span></span>
<span data-ttu-id="e02d0-136">Subdomain für die zentrale URL.</span><span class="sxs-lookup"><span data-stu-id="e02d0-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="e02d0-137">Jede Anwendung muss eine eindeutige Unterdomäne aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e02d0-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="e02d0-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="e02d0-138">-Tag</span></span>
<span data-ttu-id="e02d0-139">Viele Ressourcenkategorien für die zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="e02d0-140">-Vorlage</span><span class="sxs-lookup"><span data-stu-id="e02d0-140">-Template</span></span>
<span data-ttu-id="e02d0-141">Der Name der zentralen Anwendungsvorlage</span><span class="sxs-lookup"><span data-stu-id="e02d0-141">IoT Central application template name.</span></span>
<span data-ttu-id="e02d0-142">Standard ist eine benutzerdefinierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e02d0-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="e02d0-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e02d0-143">-Confirm</span></span>
<span data-ttu-id="e02d0-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e02d0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02d0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02d0-145">-WhatIf</span></span>
<span data-ttu-id="e02d0-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e02d0-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02d0-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e02d0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02d0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02d0-148">CommonParameters</span></span>
<span data-ttu-id="e02d0-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02d0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02d0-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02d0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02d0-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e02d0-151">INPUTS</span></span>

### <span data-ttu-id="e02d0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e02d0-152">System.String</span></span>

### <span data-ttu-id="e02d0-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e02d0-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e02d0-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e02d0-154">OUTPUTS</span></span>

### <span data-ttu-id="e02d0-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e02d0-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e02d0-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e02d0-156">NOTES</span></span>

## <span data-ttu-id="e02d0-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e02d0-157">RELATED LINKS</span></span>
