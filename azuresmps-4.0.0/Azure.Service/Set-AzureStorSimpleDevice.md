---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005959"
---
# <span data-ttu-id="a5963-101">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="a5963-101">Set-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="a5963-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5963-102">SYNOPSIS</span></span>
<span data-ttu-id="a5963-103">Ändert die Gerätekonfiguration für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="a5963-103">Changes the device configuration for a device.</span></span>

## <span data-ttu-id="a5963-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5963-104">SYNTAX</span></span>

### <span data-ttu-id="a5963-105">IdentifyByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5963-105">IdentifyByName (Default)</span></span>
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5963-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="a5963-106">IdentifyById</span></span>
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5963-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5963-107">DESCRIPTION</span></span>
<span data-ttu-id="a5963-108">Das Cmdlet " **Satz-AzureStorSimpleDevice** " ändert die Gerätekonfiguration für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="a5963-108">The **Set-AzureStorSimpleDevice** cmdlet changes the device configuration for a device.</span></span>
<span data-ttu-id="a5963-109">Wenn Sie ein Gerät zum ersten Mal einrichten, müssen Sie die Parameter *TimeZone* , *SecondaryDnsServer* und *StorSimpleNetworkConfig* angeben.</span><span class="sxs-lookup"><span data-stu-id="a5963-109">If you are setting up a device for the first time, you must specify the *TimeZone* , *SecondaryDnsServer* , and *StorSimpleNetworkConfig* parameters.</span></span>
<span data-ttu-id="a5963-110">Sie müssen die Netzwerkkonfiguration für Daten0 mit controller0 und controller1 sowie IP-Adressen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="a5963-110">You must include network configuration for Data0 with controller0 and controller1 and IP addresses.</span></span>
<span data-ttu-id="a5963-111">Es muss mindestens eine Internet-SCSI (iSCSI)-fähige Netzwerkschnittstelle vorhanden sein, um das Gerät zum ersten Mal konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="a5963-111">There must be at least one Internet SCSI (ISCSI)-enabled network interface to configure the device for the first time.</span></span>

## <span data-ttu-id="a5963-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5963-112">EXAMPLES</span></span>

### <span data-ttu-id="a5963-113">Beispiel 1: Ändern der Konfiguration für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="a5963-113">Example 1: Modify the configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="a5963-114">Der erste Befehl erstellt eine Netzwerkkonfiguration für die Daten0-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a5963-114">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="a5963-115">Mit diesem Befehl werden die *Controller0IPv4Address* -, *Controller1IPv4Address* -und *EnableIscsi* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="a5963-115">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="a5963-116">Der Befehl speichert das Ergebnis in der Variablen $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="a5963-116">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="a5963-117">Der zweite Befehl verwendet die **System. TimeZoneInfo** .NET-Klasse und die Standardsyntax, um Pacific Standard Time Zone abzurufen, und speichert dieses Objekt in der $TimeZoneInfo-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5963-117">The second command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="a5963-118">Der dritte Befehl verwendet das Cmdlet " **Get-AzureStorSimpleDevice** " und das Cmdlet " **Where-Object** Core" zum Abrufen eines Online StorSimple-Geräts und speichert es dann in der $OnlineDevice-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5963-118">The third command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="a5963-119">Der endgültige Befehl ändert die Konfiguration für das Gerät, das die angegebene Geräte-ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="a5963-119">The final command modifies the configuration for the device that has the specified device ID.</span></span>
<span data-ttu-id="a5963-120">Der Befehl verwendet das Configuration-Objekt, das das aktuelle Cmdlet im ersten Befehl erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a5963-120">The command uses the configuration object that the current cmdlet created in the first command.</span></span>
<span data-ttu-id="a5963-121">Der Befehl verwendet die in $TimeZoneInfo gespeicherte Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="a5963-121">The command uses the time zone stored in $TimeZoneInfo.</span></span>

### <span data-ttu-id="a5963-122">Beispiel 2: Rohren des Konfigurationsobjekts zum Ändern eines Geräts</span><span class="sxs-lookup"><span data-stu-id="a5963-122">Example 2: Pipe the configuration object to modify a device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="a5963-123">In diesem Beispiel wird die gleiche Konfigurationsaktualisierung wie im ersten Beispiel durchlaufen, mit der Ausnahme, dass der endgültige Befehl das Netzwerk Konfigurationsobjekt mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.</span><span class="sxs-lookup"><span data-stu-id="a5963-123">This example does the same configuration update as the first example, except that the final command passes the network configuration object to the current cmdlet by using the pipeline operator.</span></span>

### <span data-ttu-id="a5963-124">Beispiel 3: Rohren des Zeitzonenobjekts zum Ändern eines Geräts</span><span class="sxs-lookup"><span data-stu-id="a5963-124">Example 3: Pipe the time zone object to modify a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="a5963-125">In diesem Beispiel wird die gleiche Konfigurationsaktualisierung wie im ersten Beispiel durchlaufen, mit der Ausnahme, dass der endgültige Befehl das Zeitzonenobjekt mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.</span><span class="sxs-lookup"><span data-stu-id="a5963-125">This example does the same configuration update as the first example, except that the final command passes the time zone object to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="a5963-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5963-126">PARAMETERS</span></span>

### <span data-ttu-id="a5963-127">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="a5963-127">-DeviceId</span></span>
<span data-ttu-id="a5963-128">Gibt die Instanz-ID des StorSimple-Geräts an, das konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5963-128">Specifies the instance ID of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5963-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a5963-129">-DeviceName</span></span>
<span data-ttu-id="a5963-130">Gibt den Anzeigenamen des StorSimple-Geräts an, das konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5963-130">Specifies the friendly name of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5963-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a5963-131">-NewName</span></span>
<span data-ttu-id="a5963-132">Gibt den neuen Anzeigenamen des StorSimple-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a5963-132">Specifies the new friendly name of the StorSimple device.</span></span>

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

### <span data-ttu-id="a5963-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="a5963-133">-Profile</span></span>
<span data-ttu-id="a5963-134">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="a5963-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a5963-135">-SecondaryDnsServer</span><span class="sxs-lookup"><span data-stu-id="a5963-135">-SecondaryDnsServer</span></span>
<span data-ttu-id="a5963-136">Gibt einen sekundären DNS-Server für das StorSimple-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="a5963-136">Specifies a secondary DNS server for the StorSimple device.</span></span>

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

### <span data-ttu-id="a5963-137">-StorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="a5963-137">-StorSimpleNetworkConfig</span></span>
<span data-ttu-id="a5963-138">Gibt ein Array von Netzwerk Konfigurationsobjekten für Schnittstellen auf einem Gerät an.</span><span class="sxs-lookup"><span data-stu-id="a5963-138">Specifies an array of network configuration objectss for interfaces on a device.</span></span>
<span data-ttu-id="a5963-139">Verwenden Sie das New-AzureStorSimpleNetworkConfig-Cmdlet, um ein **NetworkConfig** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5963-139">To obtain a **NetworkConfig** object, use the New-AzureStorSimpleNetworkConfig cmdlet.</span></span>

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5963-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a5963-140">-TimeZone</span></span>
<span data-ttu-id="a5963-141">Gibt eine Zeitzone für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="a5963-141">Specifies a time zone for the device.</span></span>
<span data-ttu-id="a5963-142">Mit der **GetSystemTimeZone ()** -Methode können Sie ein **TimeZoneInfo** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a5963-142">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="a5963-143">Mit diesem Befehl wird beispielsweise ein Zeit Zonen Informationsobjekt für die Pazifische Standard Zeit erstellt: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="a5963-143">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5963-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5963-144">CommonParameters</span></span>
<span data-ttu-id="a5963-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5963-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5963-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5963-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5963-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5963-147">INPUTS</span></span>

### <span data-ttu-id="a5963-148">NetworkConfig, TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="a5963-148">NetworkConfig, TimeZoneInfo</span></span>
<span data-ttu-id="a5963-149">Sie können ein **NetworkConfig** -Objekt oder eine **TimeZoneInfo** -Pipeline an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="a5963-149">You can pipe a **NetworkConfig** object or a **TimeZoneInfo** to this cmdlet.</span></span>

## <span data-ttu-id="a5963-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5963-150">OUTPUTS</span></span>

### <span data-ttu-id="a5963-151">DeviceDetails</span><span class="sxs-lookup"><span data-stu-id="a5963-151">DeviceDetails</span></span>
<span data-ttu-id="a5963-152">Dieses Cmdlet gibt aktualisierte Gerätedetails für das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="a5963-152">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="a5963-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5963-153">NOTES</span></span>

## <span data-ttu-id="a5963-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5963-154">RELATED LINKS</span></span>

[<span data-ttu-id="a5963-155">Neu – AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="a5963-155">New-AzureStorSimpleNetworkConfig</span></span>](./New-AzureStorSimpleNetworkConfig.md)

[<span data-ttu-id="a5963-156">Satz-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="a5963-156">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


