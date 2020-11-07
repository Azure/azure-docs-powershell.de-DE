---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819819"
---
# <span data-ttu-id="57c24-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="57c24-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="57c24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57c24-102">SYNOPSIS</span></span>
<span data-ttu-id="57c24-103">Aktualisiert die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="57c24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57c24-104">SYNTAX</span></span>

### <span data-ttu-id="57c24-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="57c24-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c24-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c24-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57c24-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c24-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57c24-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57c24-108">DESCRIPTION</span></span>
<span data-ttu-id="57c24-109">Aktualisieren Sie die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="57c24-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57c24-110">EXAMPLES</span></span>

### <span data-ttu-id="57c24-111">Beispiel 1 Update Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="57c24-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="57c24-112">Aktualisieren Sie den Anzeigenamen in einer vorhandenen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="57c24-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="57c24-113">Example Output:</span></span>

<span data-ttu-id="57c24-114">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: der neue benutzerdefinierte Anzeige Name Unterdomäne: MyAppSubdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c24-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="57c24-115">Beispiel 2 Update-Unterdomäne</span><span class="sxs-lookup"><span data-stu-id="57c24-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="57c24-116">Aktualisieren Sie den Anzeigenamen in einer vorhandenen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="57c24-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="57c24-117">Example Output:</span></span>

<span data-ttu-id="57c24-118">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: Anzeige Name Subdomain: neue-Subdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c24-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="57c24-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="57c24-119">PARAMETERS</span></span>

### <span data-ttu-id="57c24-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57c24-120">-AsJob</span></span>
<span data-ttu-id="57c24-121">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="57c24-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="57c24-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c24-122">-DefaultProfile</span></span>
<span data-ttu-id="57c24-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57c24-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c24-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57c24-124">-DisplayName</span></span>
<span data-ttu-id="57c24-125">Benutzerdefinierter Anzeige Name der viel zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="57c24-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57c24-126">-InputObject</span></span>
<span data-ttu-id="57c24-127">Viel zentrales Anwendungs Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="57c24-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="57c24-128">-Name</span><span class="sxs-lookup"><span data-stu-id="57c24-128">-Name</span></span>
<span data-ttu-id="57c24-129">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="57c24-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="57c24-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c24-130">-ResourceGroupName</span></span>
<span data-ttu-id="57c24-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57c24-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="57c24-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="57c24-132">-ResourceId</span></span>
<span data-ttu-id="57c24-133">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="57c24-134">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="57c24-134">-Subdomain</span></span>
<span data-ttu-id="57c24-135">Unterdomäne der viel zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="57c24-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="57c24-136">-Tag</span></span>
<span data-ttu-id="57c24-137">Viele Ressourcenkategorien für die zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="57c24-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="57c24-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57c24-138">-Confirm</span></span>
<span data-ttu-id="57c24-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57c24-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c24-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c24-140">-WhatIf</span></span>
<span data-ttu-id="57c24-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57c24-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c24-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57c24-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c24-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c24-143">CommonParameters</span></span>
<span data-ttu-id="57c24-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c24-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c24-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c24-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c24-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57c24-146">INPUTS</span></span>

### <span data-ttu-id="57c24-147">System. String</span><span class="sxs-lookup"><span data-stu-id="57c24-147">System.String</span></span>

### <span data-ttu-id="57c24-148">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="57c24-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="57c24-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57c24-149">OUTPUTS</span></span>

### <span data-ttu-id="57c24-150">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="57c24-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="57c24-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="57c24-151">NOTES</span></span>

## <span data-ttu-id="57c24-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57c24-152">RELATED LINKS</span></span>
