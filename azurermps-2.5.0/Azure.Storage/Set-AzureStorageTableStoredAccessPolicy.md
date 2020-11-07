---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4d28b17146e7c4a4f4a87081b0577786b4b39930
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850952"
---
# <span data-ttu-id="36e48-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36e48-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="36e48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36e48-102">SYNOPSIS</span></span>
<span data-ttu-id="36e48-103">Legt die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle fest.</span><span class="sxs-lookup"><span data-stu-id="36e48-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e48-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36e48-105">DESCRIPTION</span></span>
<span data-ttu-id="36e48-106">Mit dem Cmdlet " **festlegen-AzureStorageTableStoredAccessPolicy** " wird die Richtlinie für den gespeicherten Zugriff für eine Azure-Speichertabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="36e48-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="36e48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36e48-107">EXAMPLES</span></span>

### <span data-ttu-id="36e48-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einer Tabelle mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="36e48-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="36e48-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen Policy08 für die Speichertabelle "MyTable" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="36e48-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="36e48-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e48-110">PARAMETERS</span></span>

### <span data-ttu-id="36e48-111">-Context</span><span class="sxs-lookup"><span data-stu-id="36e48-111">-Context</span></span>
<span data-ttu-id="36e48-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="36e48-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="36e48-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="36e48-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="36e48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e48-114">-DefaultProfile</span></span>
<span data-ttu-id="36e48-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36e48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e48-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="36e48-116">-ExpiryTime</span></span>
<span data-ttu-id="36e48-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie abläuft.</span><span class="sxs-lookup"><span data-stu-id="36e48-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="36e48-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="36e48-118">-NoExpiryTime</span></span>
<span data-ttu-id="36e48-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="36e48-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="36e48-120">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="36e48-120">-NoStartTime</span></span>
<span data-ttu-id="36e48-121">Gibt an, dass die Startzeit auf $Null festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="36e48-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="36e48-122">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="36e48-122">-Permission</span></span>
<span data-ttu-id="36e48-123">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speichertabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="36e48-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="36e48-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="36e48-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="36e48-125">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="36e48-125">-Policy</span></span>
<span data-ttu-id="36e48-126">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="36e48-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="36e48-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="36e48-127">-StartTime</span></span>
<span data-ttu-id="36e48-128">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="36e48-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="36e48-129">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="36e48-129">-Table</span></span>
<span data-ttu-id="36e48-130">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="36e48-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="36e48-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36e48-131">-Confirm</span></span>
<span data-ttu-id="36e48-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36e48-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e48-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e48-133">-WhatIf</span></span>
<span data-ttu-id="36e48-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36e48-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36e48-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36e48-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e48-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e48-136">CommonParameters</span></span>
<span data-ttu-id="36e48-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e48-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e48-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e48-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e48-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36e48-139">INPUTS</span></span>

### <span data-ttu-id="36e48-140">System. String</span><span class="sxs-lookup"><span data-stu-id="36e48-140">System.String</span></span>

### <span data-ttu-id="36e48-141">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="36e48-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="36e48-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36e48-142">OUTPUTS</span></span>

### <span data-ttu-id="36e48-143">System. String</span><span class="sxs-lookup"><span data-stu-id="36e48-143">System.String</span></span>

## <span data-ttu-id="36e48-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="36e48-144">NOTES</span></span>

## <span data-ttu-id="36e48-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36e48-145">RELATED LINKS</span></span>

[<span data-ttu-id="36e48-146">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36e48-146">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="36e48-147">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="36e48-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="36e48-148">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36e48-148">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="36e48-149">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36e48-149">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
