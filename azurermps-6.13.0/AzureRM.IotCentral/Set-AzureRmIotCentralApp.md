---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665160"
---
# <span data-ttu-id="651ee-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="651ee-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="651ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="651ee-102">SYNOPSIS</span></span>
<span data-ttu-id="651ee-103">Aktualisiert die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="651ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="651ee-104">SYNTAX</span></span>

### <span data-ttu-id="651ee-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="651ee-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="651ee-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="651ee-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="651ee-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="651ee-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="651ee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="651ee-108">DESCRIPTION</span></span>
<span data-ttu-id="651ee-109">Aktualisieren Sie die Metadaten für eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="651ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="651ee-110">EXAMPLES</span></span>

### <span data-ttu-id="651ee-111">Beispiel 1 Update Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="651ee-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="651ee-112">Aktualisieren Sie den Anzeigenamen in einer vorhandenen zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="651ee-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="651ee-113">Example Output:</span></span>

<span data-ttu-id="651ee-114">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName geben Sie Folgendes ein: Microsoft. IoTCentral/IoTApps Ort: westus-Tag: SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: der neue benutzerdefinierte Anzeige Name Unterdomäne: MyAppSubdomain-Vorlage: Abonnement-Nr iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651ee-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="651ee-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="651ee-115">PARAMETERS</span></span>

### <span data-ttu-id="651ee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="651ee-116">-AsJob</span></span>
<span data-ttu-id="651ee-117">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="651ee-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651ee-118">-DefaultProfile</span></span>
<span data-ttu-id="651ee-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="651ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="651ee-120">-DisplayName</span></span>
<span data-ttu-id="651ee-121">Benutzerdefinierter Anzeige Name der viel zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="651ee-122">-InputObject</span></span>
<span data-ttu-id="651ee-123">Viel zentrales Anwendungs Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="651ee-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-124">-Name</span><span class="sxs-lookup"><span data-stu-id="651ee-124">-Name</span></span>
<span data-ttu-id="651ee-125">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="651ee-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="651ee-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="651ee-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="651ee-128">-ResourceId</span></span>
<span data-ttu-id="651ee-129">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="651ee-130">-Tag</span></span>
<span data-ttu-id="651ee-131">Viele Ressourcenkategorien für die zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="651ee-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="651ee-132">-Confirm</span></span>
<span data-ttu-id="651ee-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="651ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="651ee-134">-WhatIf</span></span>
<span data-ttu-id="651ee-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="651ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="651ee-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="651ee-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="651ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651ee-137">CommonParameters</span></span>
<span data-ttu-id="651ee-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="651ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651ee-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651ee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651ee-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="651ee-140">INPUTS</span></span>

### <span data-ttu-id="651ee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="651ee-141">System.String</span></span>
### <span data-ttu-id="651ee-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="651ee-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="651ee-143">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="651ee-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="651ee-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="651ee-144">OUTPUTS</span></span>

### <span data-ttu-id="651ee-145">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="651ee-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="651ee-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="651ee-146">NOTES</span></span>

## <span data-ttu-id="651ee-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="651ee-147">RELATED LINKS</span></span>
