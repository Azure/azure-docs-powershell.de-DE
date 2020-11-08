---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178000"
---
# <span data-ttu-id="7ae78-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ae78-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="7ae78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ae78-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae78-103">Aktualisiert die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="7ae78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae78-104">SYNTAX</span></span>

### <span data-ttu-id="7ae78-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ae78-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ae78-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae78-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ae78-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae78-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ae78-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae78-108">DESCRIPTION</span></span>
<span data-ttu-id="7ae78-109">Aktualisieren Sie die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="7ae78-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ae78-110">EXAMPLES</span></span>

### <span data-ttu-id="7ae78-111">Beispiel 1 Update Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="7ae78-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="7ae78-112">Aktualisieren Sie den Anzeigenamen in einer vorhandenen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ae78-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="7ae78-113">Example Output:</span></span>

<span data-ttu-id="7ae78-114">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: der neue benutzerdefinierte Anzeige Name Unterdomäne: MyAppSubdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae78-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7ae78-115">Beispiel 2 Update-Unterdomäne</span><span class="sxs-lookup"><span data-stu-id="7ae78-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="7ae78-116">Aktualisieren Sie den Anzeigenamen in einer vorhandenen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ae78-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="7ae78-117">Example Output:</span></span>

<span data-ttu-id="7ae78-118">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: Anzeige Name Subdomain: neue-Subdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae78-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7ae78-119">Beispiel 3 Update-App-SKU-Informationen</span><span class="sxs-lookup"><span data-stu-id="7ae78-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="7ae78-120">Aktualisieren Sie die SKU für eine vorhandene viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ae78-121">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="7ae78-121">Example Output:</span></span>

<span data-ttu-id="7ae78-122">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: Anzeige Name Subdomain: MyAppSubdomain-Vorlage: Abonnement-Kennung: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx iotc-default@1.0.0 ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae78-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="7ae78-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae78-123">PARAMETERS</span></span>

### <span data-ttu-id="7ae78-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ae78-124">-AsJob</span></span>
<span data-ttu-id="7ae78-125">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="7ae78-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7ae78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae78-126">-DefaultProfile</span></span>
<span data-ttu-id="7ae78-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ae78-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae78-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7ae78-128">-DisplayName</span></span>
<span data-ttu-id="7ae78-129">Benutzerdefinierter Anzeige Name der viel zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="7ae78-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ae78-130">-InputObject</span></span>
<span data-ttu-id="7ae78-131">Viel zentrales Anwendungs Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="7ae78-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="7ae78-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7ae78-132">-Name</span></span>
<span data-ttu-id="7ae78-133">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="7ae78-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="7ae78-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae78-134">-ResourceGroupName</span></span>
<span data-ttu-id="7ae78-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ae78-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="7ae78-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7ae78-136">-ResourceId</span></span>
<span data-ttu-id="7ae78-137">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="7ae78-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ae78-138">-Sku</span></span>
<span data-ttu-id="7ae78-139">Preisstufe für viele zentrale Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7ae78-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="7ae78-140">Der Standardwert ist ST2.</span><span class="sxs-lookup"><span data-stu-id="7ae78-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="7ae78-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="7ae78-141">-Subdomain</span></span>
<span data-ttu-id="7ae78-142">Unterdomäne der viel zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="7ae78-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ae78-143">-Tag</span></span>
<span data-ttu-id="7ae78-144">Viele Ressourcenkategorien für die zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7ae78-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="7ae78-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ae78-145">-Confirm</span></span>
<span data-ttu-id="7ae78-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ae78-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae78-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae78-147">-WhatIf</span></span>
<span data-ttu-id="7ae78-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ae78-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ae78-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ae78-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae78-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae78-150">CommonParameters</span></span>
<span data-ttu-id="7ae78-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae78-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae78-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ae78-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae78-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ae78-153">INPUTS</span></span>

### <span data-ttu-id="7ae78-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae78-154">System.String</span></span>

### <span data-ttu-id="7ae78-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ae78-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7ae78-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ae78-156">OUTPUTS</span></span>

### <span data-ttu-id="7ae78-157">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ae78-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7ae78-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ae78-158">NOTES</span></span>

## <span data-ttu-id="7ae78-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ae78-159">RELATED LINKS</span></span>
