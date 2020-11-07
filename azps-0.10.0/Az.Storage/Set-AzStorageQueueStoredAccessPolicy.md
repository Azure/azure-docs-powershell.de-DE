---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: c6f0c713302ef8761c85da6d54404f86ff9fb814
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842868"
---
# <span data-ttu-id="6e373-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e373-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6e373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e373-102">SYNOPSIS</span></span>
<span data-ttu-id="6e373-103">Legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="6e373-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6e373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e373-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e373-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e373-105">DESCRIPTION</span></span>
<span data-ttu-id="6e373-106">Das Cmdlet " **Set-AzStorageQueueStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="6e373-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6e373-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e373-107">EXAMPLES</span></span>

### <span data-ttu-id="6e373-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6e373-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="6e373-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy07 für die Speicherwarteschlange mit dem Namen myQueue festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e373-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="6e373-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e373-110">PARAMETERS</span></span>

### <span data-ttu-id="6e373-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6e373-111">-Context</span></span>
<span data-ttu-id="6e373-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="6e373-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e373-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e373-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e373-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e373-114">-DefaultProfile</span></span>
<span data-ttu-id="6e373-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e373-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e373-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e373-116">-ExpiryTime</span></span>
<span data-ttu-id="6e373-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="6e373-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6e373-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6e373-118">-NoExpiryTime</span></span>
<span data-ttu-id="6e373-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="6e373-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6e373-120">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="6e373-120">-NoStartTime</span></span>
<span data-ttu-id="6e373-121">Gibt an, dass das Cmdlet die Startzeit auf $NULL festlegt.</span><span class="sxs-lookup"><span data-stu-id="6e373-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="6e373-122">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6e373-122">-Permission</span></span>
<span data-ttu-id="6e373-123">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6e373-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="6e373-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="6e373-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6e373-125">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6e373-125">-Policy</span></span>
<span data-ttu-id="6e373-126">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="6e373-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="6e373-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="6e373-127">-Queue</span></span>
<span data-ttu-id="6e373-128">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="6e373-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6e373-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="6e373-129">-StartTime</span></span>
<span data-ttu-id="6e373-130">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="6e373-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6e373-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e373-131">-Confirm</span></span>
<span data-ttu-id="6e373-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e373-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e373-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e373-133">-WhatIf</span></span>
<span data-ttu-id="6e373-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e373-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e373-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e373-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e373-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e373-136">CommonParameters</span></span>
<span data-ttu-id="6e373-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e373-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e373-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e373-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e373-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e373-139">INPUTS</span></span>

### <span data-ttu-id="6e373-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6e373-140">System.String</span></span>

### <span data-ttu-id="6e373-141">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e373-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e373-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e373-142">OUTPUTS</span></span>

### <span data-ttu-id="6e373-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6e373-143">System.String</span></span>

## <span data-ttu-id="6e373-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e373-144">NOTES</span></span>

## <span data-ttu-id="6e373-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e373-145">RELATED LINKS</span></span>

[<span data-ttu-id="6e373-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e373-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e373-147">Neu – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e373-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6e373-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e373-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
