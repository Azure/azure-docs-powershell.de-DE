---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 0cac398a77c6d26ed9454b7345ce1bb8fde5b965
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845264"
---
# <span data-ttu-id="03fc6-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="03fc6-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="03fc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="03fc6-103">Ruft Eigenschaften für eine oder mehrere zentrale Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="03fc6-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="03fc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03fc6-104">SYNTAX</span></span>

### <span data-ttu-id="03fc6-105">ListIotCentralAppsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03fc6-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03fc6-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fc6-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03fc6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fc6-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03fc6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03fc6-108">DESCRIPTION</span></span>
<span data-ttu-id="03fc6-109">Ruft je nach Parameter Satz die Metadaten für eine bestimmte viel zentrale Anwendung oder alle Anwendungen in einer Ressourcengruppe oder einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="03fc6-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="03fc6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03fc6-110">EXAMPLES</span></span>

### <span data-ttu-id="03fc6-111">Beispiel 1: Abrufen einer bestimmten zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="03fc6-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="03fc6-112">Ruft die Metadaten für die angegebene viel zentrale Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="03fc6-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="03fc6-113">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="03fc6-113">Example Output:</span></span>

<span data-ttu-id="03fc6-114">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="03fc6-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="03fc6-115">Beispiel 2: Abrufen von zentralen Anwendungen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03fc6-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="03fc6-116">Ruft die Metadaten für alle zentralen Anwendungen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="03fc6-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="03fc6-117">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="03fc6-117">Example Output:</span></span>

<span data-ttu-id="03fc6-118">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="03fc6-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="03fc6-119">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName2/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="03fc6-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="03fc6-120">Beispiel 3: Abrufen von zentralen Anwendungen in der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03fc6-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="03fc6-121">Ruft die Metadaten für alle zentralen Anwendungen in der bereitgestellten Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="03fc6-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="03fc6-122">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="03fc6-122">Example Output:</span></span>

<span data-ttu-id="03fc6-123">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName-Name: MyAppResourceName-Typ: Microsoft. IoTCentral/IoTApps-Standort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-DisplayName-Unterdomäne für den benutzerdefinierten Anzeige Namen: MyAppSubdomain-Vorlage: xxxxxxxx iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="03fc6-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="03fc6-124">Resourcen:/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroupName/Providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2-Name: MyAppResourceName2-Typ: Microsoft. IoTCentral/IoTApps-Ort: westus-Tag: {[Schlüssel, Val]} SKU: Microsoft. Azure. Commands. IoTCentral. Models. PSIotCentralAppSkuInfo ApplicationId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: mein benutzerdefinierter Anzeige Name 2 Subdomain: MyAppSubdomain2 Vorlage: iotc-default@1.0.0 Abonnement-Nr: xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fc6-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="03fc6-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="03fc6-125">PARAMETERS</span></span>

### <span data-ttu-id="03fc6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fc6-126">-DefaultProfile</span></span>
<span data-ttu-id="03fc6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03fc6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fc6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="03fc6-128">-Name</span></span>
<span data-ttu-id="03fc6-129">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="03fc6-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="03fc6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fc6-130">-ResourceGroupName</span></span>
<span data-ttu-id="03fc6-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03fc6-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="03fc6-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03fc6-132">-ResourceId</span></span>
<span data-ttu-id="03fc6-133">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="03fc6-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="03fc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fc6-134">CommonParameters</span></span>
<span data-ttu-id="03fc6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fc6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03fc6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fc6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03fc6-137">INPUTS</span></span>

### <span data-ttu-id="03fc6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="03fc6-138">System.String</span></span>

## <span data-ttu-id="03fc6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03fc6-139">OUTPUTS</span></span>

### <span data-ttu-id="03fc6-140">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="03fc6-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="03fc6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="03fc6-141">NOTES</span></span>

## <span data-ttu-id="03fc6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03fc6-142">RELATED LINKS</span></span>
