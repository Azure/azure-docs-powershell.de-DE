---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006057"
---
# <span data-ttu-id="679d1-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="679d1-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="679d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="679d1-102">SYNOPSIS</span></span>
<span data-ttu-id="679d1-103">Aktualisiert eine Azure Storage Access-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="679d1-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="679d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="679d1-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="679d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="679d1-105">DESCRIPTION</span></span>
<span data-ttu-id="679d1-106">Das Cmdlet " **Satz-AzureStorSimpleStorageAccountCredential** " aktualisiert eine vorhandene Azure Storage Access-Anmeldeinformationen für die Verwendung durch StorSimple OneSDK-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="679d1-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="679d1-107">Weitere Informationen dazu, wie StorSimple-Cmdlets mit Speicherkonten funktionieren, finden Sie im Hilfethema zum New-AzureStorSimpleStorageAccountCredential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679d1-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="679d1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="679d1-108">EXAMPLES</span></span>

### <span data-ttu-id="679d1-109">Beispiel 1: Ändern von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="679d1-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="679d1-110">Mit diesem Befehl werden die Speicherkonto Anmeldeinformationen mit dem Namen ContosoStorage01 so geändert, dass SSL nicht mehr erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="679d1-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="679d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="679d1-111">PARAMETERS</span></span>

### <span data-ttu-id="679d1-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="679d1-112">-Profile</span></span>
<span data-ttu-id="679d1-113">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="679d1-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="679d1-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="679d1-114">-StorageAccountKey</span></span>
<span data-ttu-id="679d1-115">Gibt die Zugriffstaste des speicherkontos als nur-Text an.</span><span class="sxs-lookup"><span data-stu-id="679d1-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d1-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="679d1-116">-StorageAccountName</span></span>
<span data-ttu-id="679d1-117">Gibt den Namen eines vorhandenen speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="679d1-117">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="679d1-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="679d1-118">-UseSSL</span></span>
<span data-ttu-id="679d1-119">Gibt an, ob SSL für die Verbindung bei Verwendung der neuen Anmeldeinformationen für das Speicherkonto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="679d1-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

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

### <span data-ttu-id="679d1-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="679d1-120">-WaitForComplete</span></span>
<span data-ttu-id="679d1-121">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="679d1-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="679d1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679d1-122">CommonParameters</span></span>
<span data-ttu-id="679d1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679d1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679d1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679d1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679d1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="679d1-125">INPUTS</span></span>

### <span data-ttu-id="679d1-126">Keine</span><span class="sxs-lookup"><span data-stu-id="679d1-126">None</span></span>

## <span data-ttu-id="679d1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="679d1-127">OUTPUTS</span></span>

### <span data-ttu-id="679d1-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="679d1-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="679d1-129">Dieses Cmdlet gibt ein **StorageAccountCredentialResponse** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="679d1-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="679d1-130">Wenn Sie diesen Parameter nicht angeben, gibt das Cmdlet ein **TaskResponse** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="679d1-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="679d1-131">Eine **StorageAccountCredentialResponse** enthält die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="679d1-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="679d1-132">**Cloudtype** ( **cloudtype** )</span><span class="sxs-lookup"><span data-stu-id="679d1-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="679d1-133">**Hostname** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="679d1-134">**InstanceId** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="679d1-135">**IsDefault** ( **boolescher** Wert)</span><span class="sxs-lookup"><span data-stu-id="679d1-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="679d1-136">**Ort** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="679d1-137">**Login** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="679d1-138">**Name** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="679d1-139">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="679d1-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="679d1-140">**Kennwort** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="679d1-141">**PasswordEncryptionCertThumbprint** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="679d1-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="679d1-142">**UseSSL** ( **boolescher Wert** )</span><span class="sxs-lookup"><span data-stu-id="679d1-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="679d1-143">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="679d1-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="679d1-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="679d1-144">NOTES</span></span>

## <span data-ttu-id="679d1-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="679d1-145">RELATED LINKS</span></span>

[<span data-ttu-id="679d1-146">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="679d1-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="679d1-147">Neu – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="679d1-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="679d1-148">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="679d1-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


