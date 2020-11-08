---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005723"
---
# <span data-ttu-id="f5748-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f5748-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="f5748-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5748-102">SYNOPSIS</span></span>
<span data-ttu-id="f5748-103">Erstellt eine Inline Speicherkonto Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="f5748-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="f5748-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5748-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5748-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5748-105">DESCRIPTION</span></span>
<span data-ttu-id="f5748-106">Mit dem Cmdlet " **New-AzureStorSimpleInlineStorageAccountCredential** " wird ein Anmeldeinformationsobjekt des Inline Azure Storage-Kontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5748-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="f5748-107">Mit diesem Cmdlet wird ein Dummy-Anmeldeinformationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5748-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="f5748-108">Sie können das Cmdlet **New-AzureStorSimpleDeviceVolumeContainer** und das aktuelle Cmdlet im gleichen Befehl mithilfe der Windows PowerShell-Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5748-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="f5748-109">Das eigentliche Speicherkonto-Anmeldeinformationsobjekt wird als Teil der Erstellung des Volumen Containers erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5748-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="f5748-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5748-110">EXAMPLES</span></span>

### <span data-ttu-id="f5748-111">Beispiel 1: Inline Erstellen einer Speicherkonto Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f5748-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="f5748-112">Dieser Befehl erstellt Inline eine Speicherkonto Anmeldeinformationen und übergibt diese dann mithilfe des Pipelineoperators an das Cmdlet **New-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="f5748-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5748-113">Dieser Container verwendet die Dummy-Anmeldeinformationen zum Erstellen eines Volumen Containers.</span><span class="sxs-lookup"><span data-stu-id="f5748-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="f5748-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5748-114">PARAMETERS</span></span>

### <span data-ttu-id="f5748-115">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="f5748-115">-Endpoint</span></span>
<span data-ttu-id="f5748-116">Gibt den Azure-Speicher Endpunkt für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="f5748-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="f5748-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5748-117">-Profile</span></span>
<span data-ttu-id="f5748-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f5748-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5748-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f5748-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5748-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5748-120">-StorageAccountKey</span></span>
<span data-ttu-id="f5748-121">Gibt den Kontoschlüssel des speicherkontos im nur-Text-Code an.</span><span class="sxs-lookup"><span data-stu-id="f5748-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="f5748-122">Der Schlüssel wird im verschlüsselten Format übertragen.</span><span class="sxs-lookup"><span data-stu-id="f5748-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5748-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f5748-123">-StorageAccountName</span></span>
<span data-ttu-id="f5748-124">Gibt den Namen eines vorhandenen speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f5748-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="f5748-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5748-125">CommonParameters</span></span>
<span data-ttu-id="f5748-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5748-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5748-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5748-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5748-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5748-128">INPUTS</span></span>

### <span data-ttu-id="f5748-129">Keine</span><span class="sxs-lookup"><span data-stu-id="f5748-129">None</span></span>

## <span data-ttu-id="f5748-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5748-130">OUTPUTS</span></span>

### <span data-ttu-id="f5748-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="f5748-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="f5748-132">Dieses Cmdlet gibt ein **cloudtype** -Objekt zurück, das die folgenden Felder enthält:</span><span class="sxs-lookup"><span data-stu-id="f5748-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="f5748-133">**Hostname**.</span><span class="sxs-lookup"><span data-stu-id="f5748-133">**Hostname**.</span></span>
<span data-ttu-id="f5748-134">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-134">**String**.</span></span> 
- <span data-ttu-id="f5748-135">**InstanceId**.</span><span class="sxs-lookup"><span data-stu-id="f5748-135">**InstanceId**.</span></span>
<span data-ttu-id="f5748-136">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-136">**String**.</span></span> 
- <span data-ttu-id="f5748-137">**IsDefault**.</span><span class="sxs-lookup"><span data-stu-id="f5748-137">**IsDefault**.</span></span>
<span data-ttu-id="f5748-138">**Boolescher Wert**.</span><span class="sxs-lookup"><span data-stu-id="f5748-138">**Boolean**.</span></span> 
- <span data-ttu-id="f5748-139">**Ort**.</span><span class="sxs-lookup"><span data-stu-id="f5748-139">**Location**.</span></span>
<span data-ttu-id="f5748-140">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-140">**String**.</span></span> 
- <span data-ttu-id="f5748-141">**Melden** Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="f5748-141">**Login**.</span></span>
<span data-ttu-id="f5748-142">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-142">**String**.</span></span> 
- <span data-ttu-id="f5748-143">**Name** aus.</span><span class="sxs-lookup"><span data-stu-id="f5748-143">**Name**.</span></span>
<span data-ttu-id="f5748-144">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-144">**String**.</span></span> 
- <span data-ttu-id="f5748-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="f5748-145">**OperationInProgress**.</span></span>
<span data-ttu-id="f5748-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="f5748-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="f5748-147">**Kennwort ein**.</span><span class="sxs-lookup"><span data-stu-id="f5748-147">**Password**.</span></span>
<span data-ttu-id="f5748-148">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-148">**String**.</span></span> 
- <span data-ttu-id="f5748-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="f5748-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="f5748-150">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5748-150">**String**.</span></span> 
- <span data-ttu-id="f5748-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="f5748-151">**UseSSL**.</span></span>
<span data-ttu-id="f5748-152">**Boolescher Wert**.</span><span class="sxs-lookup"><span data-stu-id="f5748-152">**Boolean**.</span></span> 
- <span data-ttu-id="f5748-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="f5748-153">**VolumeCount**.</span></span>
<span data-ttu-id="f5748-154">**Ganze Zahl**.</span><span class="sxs-lookup"><span data-stu-id="f5748-154">**Integer**.</span></span>

## <span data-ttu-id="f5748-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5748-155">NOTES</span></span>

## <span data-ttu-id="f5748-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5748-156">RELATED LINKS</span></span>

[<span data-ttu-id="f5748-157">Neu – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f5748-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="f5748-158">Neu – AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="f5748-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


