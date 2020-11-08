---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006655"
---
# <span data-ttu-id="8813f-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8813f-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="8813f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8813f-102">SYNOPSIS</span></span>
<span data-ttu-id="8813f-103">Löscht eine vorhandene Speicherkonto Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="8813f-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="8813f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8813f-104">SYNTAX</span></span>

### <span data-ttu-id="8813f-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="8813f-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8813f-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="8813f-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8813f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8813f-107">DESCRIPTION</span></span>
<span data-ttu-id="8813f-108">Das Cmdlet **Remove-AzureStorSimpleStorageAccountCredential** löscht eine vorhandene Speicherkonto Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="8813f-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="8813f-109">Geben Sie ein Konto nach Namen an, oder verwenden Sie das Cmdlet " **Get-AzureStorSimpleStorageAccountCredential** ", um ein **StorageAccountCredential** -Objekt zum Löschen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8813f-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="8813f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8813f-110">EXAMPLES</span></span>

### <span data-ttu-id="8813f-111">Beispiel 1: Entfernen der Anmeldeinformationen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8813f-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="8813f-112">Dieser Befehl entfernt die Kontoanmeldeinformationen für das Speicherkonto mit dem Namen ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="8813f-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="8813f-113">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8813f-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8813f-114">Das Cmdlet entfernt die Anmeldeinformationen, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8813f-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="8813f-115">Beispiel 2: Entfernen der Anmeldeinformationen eines speicherkontos mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="8813f-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="8813f-116">Dieser Befehl ruft das Speicherkonto mit dem Namen ContosoStorage07 mit dem Cmdlet **Get-AzureStorSimpleStorageAccountCredential** ab und übergibt dieses Objekt dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8813f-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="8813f-117">Das aktuelle Cmdlet entfernt die Anmeldeinformationen für dieses Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="8813f-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="8813f-118">Mit diesem Befehl wird der *WaitForComplete* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8813f-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="8813f-119">Das Cmdlet gibt erst dann die Steuerung an die Konsole zurück, wenn der Löschvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8813f-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="8813f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8813f-120">PARAMETERS</span></span>

### <span data-ttu-id="8813f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8813f-121">-Force</span></span>
<span data-ttu-id="8813f-122">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8813f-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="8813f-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="8813f-123">-Profile</span></span>
<span data-ttu-id="8813f-124">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="8813f-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8813f-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="8813f-125">-SAC</span></span>
<span data-ttu-id="8813f-126">Gibt Anmeldeinformationen als **StorageAccountCredential** -Objekt an, um Sie zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8813f-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="8813f-127">Verwenden Sie das Cmdlet **Get-AzureStorSimpleStorageAccountCredential** , um ein **StorageAccountCredential** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8813f-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8813f-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8813f-128">-StorageAccountName</span></span>
<span data-ttu-id="8813f-129">Gibt den Namen der zu löschenden Speicherkonto Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="8813f-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8813f-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8813f-130">-WaitForComplete</span></span>
<span data-ttu-id="8813f-131">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8813f-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8813f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8813f-132">CommonParameters</span></span>
<span data-ttu-id="8813f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8813f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8813f-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8813f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8813f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8813f-135">INPUTS</span></span>

### <span data-ttu-id="8813f-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8813f-136">StorageAccountCredential</span></span>
<span data-ttu-id="8813f-137">Dieses Cmdlet akzeptiert ein **StorageAccountCredential** -Objekt mithilfe der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8813f-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="8813f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8813f-138">OUTPUTS</span></span>

### <span data-ttu-id="8813f-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="8813f-139">TaskStatusInfo</span></span>
<span data-ttu-id="8813f-140">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="8813f-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="8813f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="8813f-141">NOTES</span></span>

## <span data-ttu-id="8813f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8813f-142">RELATED LINKS</span></span>

[<span data-ttu-id="8813f-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8813f-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8813f-144">Neu – AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8813f-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8813f-145">Satz-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8813f-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8813f-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="8813f-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


