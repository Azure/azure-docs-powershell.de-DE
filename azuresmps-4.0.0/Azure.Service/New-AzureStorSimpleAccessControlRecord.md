---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006416"
---
# <span data-ttu-id="6309e-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6309e-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="6309e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6309e-102">SYNOPSIS</span></span>
<span data-ttu-id="6309e-103">Erstellt einen Zugriffssteuerungseintrag.</span><span class="sxs-lookup"><span data-stu-id="6309e-103">Creates an access control record.</span></span>

## <span data-ttu-id="6309e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6309e-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6309e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6309e-105">DESCRIPTION</span></span>
<span data-ttu-id="6309e-106">Das Cmdlet **New-AzureStorSimpleAccessControlRecord** erstellt einen Zugriffssteuerungseintrag.</span><span class="sxs-lookup"><span data-stu-id="6309e-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="6309e-107">Sie können ein **AccessControlRecord** -Objekt verwenden, um Volumes zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6309e-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="6309e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6309e-108">EXAMPLES</span></span>

### <span data-ttu-id="6309e-109">Beispiel 1: Erstellen eines Zugriffs Controlaccess-Steuerelement Eintrags und warten auf das resultaccess-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6309e-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="6309e-110">Dieser Befehl erstellt einen Zugriffssteuerungseintrag mit dem Namen Acr10 für den iSCSI-Initiator mit dem Namen Iqn10.</span><span class="sxs-lookup"><span data-stu-id="6309e-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="6309e-111">Dieser Befehl gibt den *WaitForComplete* -Parameter an, und der Befehl wartet daher, bis der Vorgang abgeschlossen ist, und gibt dann ein **TaskStatusInfo** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6309e-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="6309e-112">Beispiel 2: Erstellen eines Access Controlaccess Control recordaccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="6309e-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="6309e-113">Dieser Befehl erstellt einen Zugriffssteuerungseintrag mit dem Namen Acr11 für den iSCSI-Initiator mit dem Namen Iqn11.</span><span class="sxs-lookup"><span data-stu-id="6309e-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="6309e-114">Mit diesem Befehl wird der *WaitForComplete* -Parameter nicht angegeben, und daher wird der Befehl von der Aufgabe gestartet und dann ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6309e-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="6309e-115">Verwenden Sie das Cmdlet **Get-AzureStorSimpleTask** , um den Status der Aufgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6309e-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="6309e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6309e-116">PARAMETERS</span></span>

### <span data-ttu-id="6309e-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="6309e-117">-ACRName</span></span>
<span data-ttu-id="6309e-118">Gibt einen Namen für den Zugriffssteuerungseintrag an.</span><span class="sxs-lookup"><span data-stu-id="6309e-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="6309e-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="6309e-119">-IQNInitiatorName</span></span>
<span data-ttu-id="6309e-120">Gibt den iSCSI Qualified Name (IQN) des iSCSI-Initiators an, dem dieses Cmdlet Zugriff auf das Volume gewährt.</span><span class="sxs-lookup"><span data-stu-id="6309e-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6309e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6309e-121">-Profile</span></span>
<span data-ttu-id="6309e-122">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="6309e-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6309e-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6309e-123">-WaitForComplete</span></span>
<span data-ttu-id="6309e-124">Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6309e-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="6309e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6309e-125">CommonParameters</span></span>
<span data-ttu-id="6309e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6309e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6309e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6309e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6309e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6309e-128">INPUTS</span></span>

### <span data-ttu-id="6309e-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6309e-129">None</span></span>

## <span data-ttu-id="6309e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6309e-130">OUTPUTS</span></span>

### <span data-ttu-id="6309e-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="6309e-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="6309e-132">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6309e-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="6309e-133">Wenn Sie diesen Parameter nicht angeben, wird ein **TaskResponse** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6309e-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="6309e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6309e-134">NOTES</span></span>

## <span data-ttu-id="6309e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6309e-135">RELATED LINKS</span></span>

[<span data-ttu-id="6309e-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6309e-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6309e-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6309e-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6309e-138">Satz-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6309e-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6309e-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6309e-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


