---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32ba9d7c10b80eee23c2d41ec48eac4c01239681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658744"
---
# <span data-ttu-id="ac786-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac786-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ac786-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac786-102">SYNOPSIS</span></span>
<span data-ttu-id="ac786-103">Legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="ac786-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ac786-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac786-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac786-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac786-105">DESCRIPTION</span></span>
<span data-ttu-id="ac786-106">Das Cmdlet " **Set-AzStorageQueueStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="ac786-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ac786-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac786-107">EXAMPLES</span></span>

### <span data-ttu-id="ac786-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ac786-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="ac786-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy07 für die Speicherwarteschlange mit dem Namen myQueue festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac786-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="ac786-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac786-110">PARAMETERS</span></span>

### <span data-ttu-id="ac786-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ac786-111">-Context</span></span>
<span data-ttu-id="ac786-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ac786-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ac786-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac786-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac786-114">-DefaultProfile</span></span>
<span data-ttu-id="ac786-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac786-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ac786-116">-ExpiryTime</span></span>
<span data-ttu-id="ac786-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="ac786-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ac786-118">-NoExpiryTime</span></span>
<span data-ttu-id="ac786-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="ac786-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-120">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="ac786-120">-NoStartTime</span></span>
<span data-ttu-id="ac786-121">Gibt an, dass das Cmdlet die Startzeit auf $NULL festlegt.</span><span class="sxs-lookup"><span data-stu-id="ac786-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-122">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ac786-122">-Permission</span></span>
<span data-ttu-id="ac786-123">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ac786-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="ac786-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="ac786-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-125">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ac786-125">-Policy</span></span>
<span data-ttu-id="ac786-126">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="ac786-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="ac786-127">-Queue</span></span>
<span data-ttu-id="ac786-128">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="ac786-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ac786-129">-StartTime</span></span>
<span data-ttu-id="ac786-130">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="ac786-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac786-131">-Confirm</span></span>
<span data-ttu-id="ac786-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac786-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac786-133">-WhatIf</span></span>
<span data-ttu-id="ac786-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac786-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac786-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac786-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac786-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac786-136">CommonParameters</span></span>
<span data-ttu-id="ac786-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac786-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac786-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac786-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac786-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac786-139">INPUTS</span></span>

### <span data-ttu-id="ac786-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ac786-140">System.String</span></span>

### <span data-ttu-id="ac786-141">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac786-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac786-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac786-142">OUTPUTS</span></span>

### <span data-ttu-id="ac786-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ac786-143">System.String</span></span>

## <span data-ttu-id="ac786-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac786-144">NOTES</span></span>

## <span data-ttu-id="ac786-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac786-145">RELATED LINKS</span></span>

[<span data-ttu-id="ac786-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac786-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac786-147">Neu – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac786-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac786-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac786-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
