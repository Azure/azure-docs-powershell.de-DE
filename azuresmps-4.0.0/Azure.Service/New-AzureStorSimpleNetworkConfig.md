---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005721"
---
# <span data-ttu-id="9298a-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="9298a-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="9298a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9298a-102">SYNOPSIS</span></span>
<span data-ttu-id="9298a-103">Bereitet ein Netzwerk Konfigurationsobjekt vor.</span><span class="sxs-lookup"><span data-stu-id="9298a-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="9298a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9298a-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9298a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9298a-105">DESCRIPTION</span></span>
<span data-ttu-id="9298a-106">Mit dem Cmdlet **New-AzureStorSimpleNetworkConfig** wird ein Netzwerk Konfigurationsobjekt für die Übergabe an das Cmdlet " **Satz-AzureStorSimpleDevice** " vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="9298a-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="9298a-107">Setzen Sie den *Controller0IPAddress* -Parameter und den *Controller1IPAddress* -Parameter nur auf der Daten0-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9298a-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="9298a-108">Daten0 unterstützt nur drei Einstellungen: *Controller0IPAddress* , *Controller1IPAdress* und *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="9298a-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="9298a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9298a-109">EXAMPLES</span></span>

### <span data-ttu-id="9298a-110">Beispiel 1: Konfigurieren einer Daten0-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9298a-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="9298a-111">Dieser Befehl erstellt die Netzwerkkonfiguration für die Daten0-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9298a-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="9298a-112">Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9298a-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="9298a-113">Dieses Cmdlet kann Daten0 nur für diese drei Parameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9298a-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="9298a-114">Beispiel 2: Konfigurieren einer anderen Schnittstelle als Daten0</span><span class="sxs-lookup"><span data-stu-id="9298a-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="9298a-115">Dieser Befehl konfiguriert die data1-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9298a-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="9298a-116">Beispiel 3: Ändern einer Konfiguration für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="9298a-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="9298a-117">Der erste Befehl erstellt eine Netzwerkkonfiguration für die Daten0-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9298a-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="9298a-118">Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9298a-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="9298a-119">Der Befehl speichert das Ergebnis in der Variablen $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="9298a-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="9298a-120">Der zweite Befehl verwendet das Cmdlet " **Get-AzureStorSimpleDevice** " und das Cmdlet " **Where-Object** Core" zum Abrufen eines Online StorSimple-Geräts und speichert es dann in der $OnlineDevice-Variablen.</span><span class="sxs-lookup"><span data-stu-id="9298a-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="9298a-121">Der endgültige Befehl ändert die Konfiguration für das Gerät, das über die angegebene Geräte-ID verfügt, mithilfe des Cmdlets " **festgelegt-AzureStorSimpleDevice** ".</span><span class="sxs-lookup"><span data-stu-id="9298a-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="9298a-122">Der Befehl verwendet das Configuration-Objekt, das das aktuelle Cmdlet im ersten Befehl erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="9298a-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="9298a-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="9298a-123">PARAMETERS</span></span>

### <span data-ttu-id="9298a-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="9298a-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="9298a-125">Gibt die IPv4-Adresse für Controller 0 an.</span><span class="sxs-lookup"><span data-stu-id="9298a-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="9298a-126">Geben Sie diesen Parameter nur für die Daten0-Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-126">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="9298a-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="9298a-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="9298a-128">Gibt die IPv4-Adresse für Controller 1 an.</span><span class="sxs-lookup"><span data-stu-id="9298a-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="9298a-129">Geben Sie diesen Parameter nur für die Daten0-Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-129">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="9298a-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="9298a-130">-EnableCloud</span></span>
<span data-ttu-id="9298a-131">Gibt an, ob die Benutzeroberfläche in der Cloud aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9298a-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298a-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="9298a-132">-EnableIscsi</span></span>
<span data-ttu-id="9298a-133">Gibt an, ob Internet SCSI (iSCSI) für die Schnittstelle aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9298a-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298a-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="9298a-134">-InterfaceAlias</span></span>
<span data-ttu-id="9298a-135">Gibt den Schnittstellen Alias der Schnittstelle an, für die dieses Cmdlet Einstellungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9298a-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="9298a-136">Gültige Werte sind von Daten0 bis Daten5.</span><span class="sxs-lookup"><span data-stu-id="9298a-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298a-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="9298a-137">-IPv4Address</span></span>
<span data-ttu-id="9298a-138">Gibt die IPv4-Adresse für die Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-138">Specifies the IPv4 address for the interface.</span></span>

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

### <span data-ttu-id="9298a-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="9298a-139">-IPv4Gateway</span></span>
<span data-ttu-id="9298a-140">Gibt die IPv4-Adresse eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="9298a-140">Specifies the IPv4 address of a gateway.</span></span>

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

### <span data-ttu-id="9298a-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="9298a-141">-IPv4Netmask</span></span>
<span data-ttu-id="9298a-142">Gibt die IPv4-Netzmaske für die Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-142">Specifies the IPv4 netmask for the interface.</span></span>

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

### <span data-ttu-id="9298a-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="9298a-143">-IPv6Gateway</span></span>
<span data-ttu-id="9298a-144">Gibt das IPv6-Gateway für die Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-144">Specifies the IPv6 gateway for the interface.</span></span>

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

### <span data-ttu-id="9298a-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="9298a-145">-IPv6Prefix</span></span>
<span data-ttu-id="9298a-146">Gibt das IPv6-Präfix für die Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="9298a-146">Specifies the IPv6 prefix for the interface.</span></span>

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

### <span data-ttu-id="9298a-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="9298a-147">-Profile</span></span>
<span data-ttu-id="9298a-148">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="9298a-148">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9298a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9298a-149">CommonParameters</span></span>
<span data-ttu-id="9298a-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9298a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9298a-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9298a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9298a-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9298a-152">INPUTS</span></span>

### <span data-ttu-id="9298a-153">Keine</span><span class="sxs-lookup"><span data-stu-id="9298a-153">None</span></span>

## <span data-ttu-id="9298a-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9298a-154">OUTPUTS</span></span>

### <span data-ttu-id="9298a-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="9298a-155">NetworkConfig</span></span>
<span data-ttu-id="9298a-156">Dieses Cmdlet gibt ein NetworkConfig-Objekt zurück, das die folgenden Eigenschaften enthält:</span><span class="sxs-lookup"><span data-stu-id="9298a-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="9298a-157">**IsIscsiEnabled** ( **boolescher Wert** )</span><span class="sxs-lookup"><span data-stu-id="9298a-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="9298a-158">**IsCloudEnabled** ( **boolescher Wert** )</span><span class="sxs-lookup"><span data-stu-id="9298a-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="9298a-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-163">**IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-164">**IPv6Prefix** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="9298a-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="9298a-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="9298a-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="9298a-166">**InterfaceAlias** ( **netinterface-Schnittstelle** )</span><span class="sxs-lookup"><span data-stu-id="9298a-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="9298a-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="9298a-167">NOTES</span></span>

## <span data-ttu-id="9298a-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9298a-168">RELATED LINKS</span></span>

[<span data-ttu-id="9298a-169">Satz-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="9298a-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="9298a-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="9298a-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


