---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005641"
---
# <span data-ttu-id="ed7da-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="ed7da-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="ed7da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed7da-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7da-103">Erstellt oder aktualisiert die Gerätekonfiguration eines virtuellen StorSimple-Geräts.</span><span class="sxs-lookup"><span data-stu-id="ed7da-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="ed7da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7da-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed7da-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed7da-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7da-106">Das Cmdlet " **Satz-AzureStorSimpleVirtualDevice** " erstellt oder aktualisiert die Gerätekonfiguration eines virtuellen Azure StorSimple-Geräts.</span><span class="sxs-lookup"><span data-stu-id="ed7da-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="ed7da-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed7da-107">EXAMPLES</span></span>

### <span data-ttu-id="ed7da-108">Beispiel 1: Aktualisieren eines virtuellen Geräts</span><span class="sxs-lookup"><span data-stu-id="ed7da-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="ed7da-109">Der erste Befehl verwendet die **System. TimeZoneInfo** .NET-Klasse und die Standardsyntax, um Pacific Standard Time Zone abzurufen, und speichert dieses Objekt in der $TimeZoneInfo-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ed7da-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="ed7da-110">Der zweite Befehl aktualisiert das Gerät mit dem Namen Contoso23, um die in $TimeZoneInfo angegebene Zeitzone zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed7da-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="ed7da-111">Für den Zugriff auf die Konfiguration des virtuellen Geräts benötigt der Befehl den geheimen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed7da-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="ed7da-112">Beispiel 2: Aktualisieren eines virtuellen Geräts mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="ed7da-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="ed7da-113">Dieser Befehl aktualisiert das Gerät mit dem Namen Contoso23, um die vom Befehl erstellte Zeitzone zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed7da-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="ed7da-114">Für den Zugriff auf die Konfiguration des virtuellen Geräts benötigt der Befehl den geheimen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ed7da-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="ed7da-115">Dieser Befehl funktioniert auf die gleiche Weise wie im vorherigen Beispiel, mit der Ausnahme, dass er die Zeitzone mithilfe des Pipelineoperators an das aktuelle Cmdlet übergibt.</span><span class="sxs-lookup"><span data-stu-id="ed7da-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="ed7da-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed7da-116">PARAMETERS</span></span>

### <span data-ttu-id="ed7da-117">-Administrator Password</span><span class="sxs-lookup"><span data-stu-id="ed7da-117">-AdministratorPassword</span></span>
<span data-ttu-id="ed7da-118">Gibt das Administratorkennwort des virtuellen Geräts an, das konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed7da-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="ed7da-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ed7da-119">-DeviceName</span></span>
<span data-ttu-id="ed7da-120">Gibt den Namen des virtuellen Geräts an, das konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed7da-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="ed7da-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed7da-121">-Profile</span></span>
<span data-ttu-id="ed7da-122">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="ed7da-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ed7da-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="ed7da-123">-SecretKey</span></span>
<span data-ttu-id="ed7da-124">Gibt einen Dienst Verschlüsselungsschlüssel für das virtuelle Gerät an.</span><span class="sxs-lookup"><span data-stu-id="ed7da-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="ed7da-125">Dieser Schlüssel wird generiert, wenn das erste physische Gerät bei einer Ressource registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ed7da-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="ed7da-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="ed7da-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="ed7da-127">Gibt das Kennwort des Snapshot-Managers an.</span><span class="sxs-lookup"><span data-stu-id="ed7da-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="ed7da-128">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ed7da-128">-TimeZone</span></span>
<span data-ttu-id="ed7da-129">Gibt eine Zeitzone für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="ed7da-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="ed7da-130">Mit der **GetSystemTimeZone ()** -Methode können Sie ein **TimeZoneInfo** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed7da-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="ed7da-131">Mit diesem Befehl wird beispielsweise ein Zeit Zonen Informationsobjekt für die Pazifische Standard Zeit erstellt: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="ed7da-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

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

### <span data-ttu-id="ed7da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7da-132">CommonParameters</span></span>
<span data-ttu-id="ed7da-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7da-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7da-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7da-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed7da-135">INPUTS</span></span>

### <span data-ttu-id="ed7da-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="ed7da-136">TimeZoneInfo</span></span>
<span data-ttu-id="ed7da-137">Sie können ein **TimeZoneInfo** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="ed7da-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="ed7da-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed7da-138">OUTPUTS</span></span>

### <span data-ttu-id="ed7da-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="ed7da-139">DeviceJobDetails</span></span>
<span data-ttu-id="ed7da-140">Dieses Cmdlet gibt aktualisierte Gerätedetails für das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="ed7da-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="ed7da-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed7da-141">NOTES</span></span>

## <span data-ttu-id="ed7da-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed7da-142">RELATED LINKS</span></span>

[<span data-ttu-id="ed7da-143">Neu – AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="ed7da-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="ed7da-144">Satz-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="ed7da-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


