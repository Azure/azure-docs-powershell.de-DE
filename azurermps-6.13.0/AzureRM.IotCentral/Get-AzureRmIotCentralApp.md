---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665161"
---
# <span data-ttu-id="a27c2-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a27c2-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="a27c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a27c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a27c2-103">Ruft Eigenschaften für eine oder mehrere zentrale Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="a27c2-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a27c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a27c2-104">SYNTAX</span></span>

### <span data-ttu-id="a27c2-105">ListIotCentralAppsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a27c2-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a27c2-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="a27c2-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27c2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a27c2-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a27c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a27c2-108">DESCRIPTION</span></span>
<span data-ttu-id="a27c2-109">Ruft je nach Parameter Satz die Metadaten für eine bestimmte viel zentrale Anwendung oder alle Anwendungen in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a27c2-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="a27c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a27c2-110">EXAMPLES</span></span>

### <span data-ttu-id="a27c2-111">Beispiel 1: Abrufen einer bestimmten zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a27c2-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="a27c2-112">Ruft die Metadaten für die angegebene viel zentrale Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="a27c2-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="a27c2-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="a27c2-113">Example Output:</span></span>

<span data-ttu-id="a27c2-114">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="a27c2-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="a27c2-115">Beispiel 2: Abrufen von zentralen Anwendungen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a27c2-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="a27c2-116">Ruft die Metadaten für alle zentralen Anwendungen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a27c2-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="a27c2-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="a27c2-117">Example Output:</span></span>

<span data-ttu-id="a27c2-118">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="a27c2-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="a27c2-119">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName2/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="a27c2-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="a27c2-120">Beispiel 3: Abrufen von zentralen Anwendungen in der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a27c2-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="a27c2-121">Ruft die Metadaten für alle zentralen Anwendungen in der bereitgestellten Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a27c2-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="a27c2-122">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="a27c2-122">Example Output:</span></span>

<span data-ttu-id="a27c2-123">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="a27c2-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="a27c2-124">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27c2-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="a27c2-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="a27c2-125">PARAMETERS</span></span>

### <span data-ttu-id="a27c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27c2-126">-DefaultProfile</span></span>
<span data-ttu-id="a27c2-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a27c2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27c2-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a27c2-128">-Name</span></span>
<span data-ttu-id="a27c2-129">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="a27c2-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="a27c2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27c2-130">-ResourceGroupName</span></span>
<span data-ttu-id="a27c2-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a27c2-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a27c2-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a27c2-132">-ResourceId</span></span>
<span data-ttu-id="a27c2-133">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a27c2-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="a27c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27c2-134">CommonParameters</span></span>
<span data-ttu-id="a27c2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27c2-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a27c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27c2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a27c2-137">INPUTS</span></span>

### <span data-ttu-id="a27c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a27c2-138">System.String</span></span>
## <span data-ttu-id="a27c2-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a27c2-139">OUTPUTS</span></span>

### <span data-ttu-id="a27c2-140">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a27c2-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="a27c2-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a27c2-141">NOTES</span></span>

## <span data-ttu-id="a27c2-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a27c2-142">RELATED LINKS</span></span>
