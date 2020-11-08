---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005726"
---
# <span data-ttu-id="4bfa9-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="4bfa9-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="4bfa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfa9-103">Erstellt einen Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-103">Creates a volume container.</span></span>

## <span data-ttu-id="4bfa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bfa9-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bfa9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="4bfa9-106">Das Cmdlet **New-AzureStorSimpleDeviceVolumeContainer** erstellt einen Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="4bfa9-107">Sie müssen dem neuen Volumen Container eine Speicherkonto Anmeldeinformationen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="4bfa9-108">Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um die Anmeldeinformationen eines speicherkontos zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="4bfa9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bfa9-109">EXAMPLES</span></span>

### <span data-ttu-id="4bfa9-110">Beispiel 1: Erstellen eines Containers</span><span class="sxs-lookup"><span data-stu-id="4bfa9-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="4bfa9-111">Dieser Befehl ruft die Speicherkonto Anmeldeinformationen für das Konto mit dem Namen ContosoAccount mit dem Cmdlet **Get-AzureStorSimpleStorageAccountCredential** ab.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="4bfa9-112">Der Befehl übergibt die Anmeldeinformationen mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4bfa9-113">Dieses Cmdlet verwendet die Anmeldeinformationen dieses Cmdlets, um den Container mit dem Namen Container08 auf dem Gerät mit dem Namen Contoso63-AppVm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="4bfa9-114">Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="4bfa9-115">Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="4bfa9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bfa9-116">PARAMETERS</span></span>

### <span data-ttu-id="4bfa9-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="4bfa9-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="4bfa9-118">Gibt die Bandbreiten Rate in Megabit pro Sekunde (Mbit/s) an.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfa9-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4bfa9-119">-DeviceName</span></span>
<span data-ttu-id="4bfa9-120">Gibt den Namen des StorSimple-Geräts an, auf dem der Volumen Container erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="4bfa9-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="4bfa9-121">-EncryptionEnabled</span></span>
<span data-ttu-id="4bfa9-122">Gibt an, ob die Verschlüsselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="4bfa9-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4bfa9-123">-EncryptionKey</span></span>
<span data-ttu-id="4bfa9-124">Gibt den Verschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="4bfa9-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4bfa9-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="4bfa9-126">Gibt die Anmeldeinformationen als **StorageAccountCredential** -Objekt an, das dem neuen Volumen Container zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="4bfa9-127">Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um ein **StorageAccountCredential** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfa9-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="4bfa9-128">-Profile</span></span>
<span data-ttu-id="4bfa9-129">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4bfa9-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="4bfa9-130">-VolumeContainerName</span></span>
<span data-ttu-id="4bfa9-131">Gibt den Namen des zu erstellende Volumen Containers an.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-131">Specifies the name of the volume container to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfa9-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="4bfa9-132">-WaitForComplete</span></span>
<span data-ttu-id="4bfa9-133">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="4bfa9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfa9-134">CommonParameters</span></span>
<span data-ttu-id="4bfa9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfa9-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bfa9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfa9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bfa9-137">INPUTS</span></span>

### <span data-ttu-id="4bfa9-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4bfa9-138">StorageAccountCredential</span></span>
<span data-ttu-id="4bfa9-139">Dieses Cmdlet akzeptiert ein **PrimaryStorageAccountCredential** -Objekt, das dem Volumen Container zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="4bfa9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bfa9-140">OUTPUTS</span></span>

### <span data-ttu-id="4bfa9-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="4bfa9-141">TaskStatusInfo</span></span>
<span data-ttu-id="4bfa9-142">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4bfa9-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="4bfa9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bfa9-143">NOTES</span></span>

## <span data-ttu-id="4bfa9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bfa9-144">RELATED LINKS</span></span>

[<span data-ttu-id="4bfa9-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="4bfa9-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="4bfa9-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="4bfa9-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="4bfa9-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4bfa9-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="4bfa9-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="4bfa9-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


