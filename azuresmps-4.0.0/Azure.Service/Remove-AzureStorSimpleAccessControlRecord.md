---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006302"
---
# <span data-ttu-id="cdb93-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="cdb93-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="cdb93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdb93-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb93-103">Löscht einen Zugriffssteuerungseintrag aus der Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cdb93-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="cdb93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdb93-104">SYNTAX</span></span>

### <span data-ttu-id="cdb93-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="cdb93-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdb93-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="cdb93-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cdb93-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdb93-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb93-108">Das Cmdlet **Remove-AzureStorSimpleAccessControlRecord** löscht einen Zugriffssteuerungseintrag aus der Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cdb93-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="cdb93-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdb93-109">EXAMPLES</span></span>

### <span data-ttu-id="cdb93-110">Beispiel 1: Entfernen eines Access Controlaccess Control recordaccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="cdb93-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="cdb93-111">Dieser Befehl löscht den Zugriffssteuerungseintrag mit dem Namen Acr10.</span><span class="sxs-lookup"><span data-stu-id="cdb93-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="cdb93-112">Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cdb93-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="cdb93-113">Beispiel 2: Entfernen eines Access-Controlaccess-Steuerelement Eintrags mithilfe des pipelineAccess Controlaccess Controlaccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="cdb93-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="cdb93-114">Dieser Befehl verwendet die **Get-AzureStorSimpleAccessControlRecord-** Funktion, um die **AccessControlRecord** mit dem Namen Acr10 abzurufen, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb93-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cdb93-115">Der Befehl startet den Vorgang, der das **AccessControlRecord** -Objekt entfernt, und gibt dann ein **TaskResponse** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cdb93-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="cdb93-116">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cdb93-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="cdb93-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdb93-117">PARAMETERS</span></span>

### <span data-ttu-id="cdb93-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="cdb93-118">-ACR</span></span>
<span data-ttu-id="cdb93-119">Gibt ein **AccessControlRecord** -Objekt an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cdb93-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="cdb93-120">Verwenden Sie das Cmdlet **Get-AzureStorSimpleAccessControlRecord** , um ein **AccessControlRecord** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cdb93-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb93-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="cdb93-121">-ACRName</span></span>
<span data-ttu-id="cdb93-122">Gibt den Namen des zu löschenden Zugriffssteuerungseintrags an.</span><span class="sxs-lookup"><span data-stu-id="cdb93-122">Specifies a name of the access control record to delete.</span></span>

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

### <span data-ttu-id="cdb93-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb93-123">-Force</span></span>
<span data-ttu-id="cdb93-124">Gibt an, dass Sie von diesem Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="cdb93-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="cdb93-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="cdb93-125">-Profile</span></span>
<span data-ttu-id="cdb93-126">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="cdb93-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cdb93-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="cdb93-127">-WaitForComplete</span></span>
<span data-ttu-id="cdb93-128">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cdb93-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="cdb93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb93-129">CommonParameters</span></span>
<span data-ttu-id="cdb93-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb93-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb93-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb93-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdb93-132">INPUTS</span></span>

### <span data-ttu-id="cdb93-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="cdb93-133">AccessControlRecord</span></span>
<span data-ttu-id="cdb93-134">Dieses Cmdlet akzeptiert ein **AccessControlRecord** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdb93-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="cdb93-135">Ein **AccessControlRecord** -Objekt enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="cdb93-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="cdb93-136">**Global** -Nr ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="cdb93-137">**Initiatorname** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="cdb93-138">**InstanceId** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="cdb93-139">**Name** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="cdb93-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="cdb93-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="cdb93-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="cdb93-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdb93-142">OUTPUTS</span></span>

### <span data-ttu-id="cdb93-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="cdb93-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="cdb93-144">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="cdb93-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="cdb93-145">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdb93-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="cdb93-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdb93-146">NOTES</span></span>

## <span data-ttu-id="cdb93-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdb93-147">RELATED LINKS</span></span>

[<span data-ttu-id="cdb93-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="cdb93-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="cdb93-149">Neu – AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="cdb93-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="cdb93-150">Satz-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="cdb93-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="cdb93-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="cdb93-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


