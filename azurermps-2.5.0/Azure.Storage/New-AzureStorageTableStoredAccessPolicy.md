---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850503"
---
# <span data-ttu-id="93966-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93966-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="93966-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93966-102">SYNOPSIS</span></span>
<span data-ttu-id="93966-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="93966-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93966-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93966-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93966-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93966-105">DESCRIPTION</span></span>
<span data-ttu-id="93966-106">Das Cmdlet **New-AzureStorageTableStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="93966-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="93966-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93966-107">EXAMPLES</span></span>

### <span data-ttu-id="93966-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="93966-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="93966-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy02 in der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="93966-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="93966-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93966-110">PARAMETERS</span></span>

### <span data-ttu-id="93966-111">-Context</span><span class="sxs-lookup"><span data-stu-id="93966-111">-Context</span></span>
<span data-ttu-id="93966-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="93966-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="93966-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93966-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="93966-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93966-114">-DefaultProfile</span></span>
<span data-ttu-id="93966-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93966-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93966-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="93966-116">-ExpiryTime</span></span>
<span data-ttu-id="93966-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="93966-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="93966-118">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="93966-118">-Permission</span></span>
<span data-ttu-id="93966-119">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speichertabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="93966-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="93966-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="93966-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="93966-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="93966-121">-Policy</span></span>
<span data-ttu-id="93966-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="93966-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="93966-123">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="93966-123">-StartTime</span></span>
<span data-ttu-id="93966-124">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="93966-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="93966-125">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="93966-125">-Table</span></span>
<span data-ttu-id="93966-126">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="93966-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="93966-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93966-127">CommonParameters</span></span>
<span data-ttu-id="93966-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93966-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93966-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93966-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93966-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93966-130">INPUTS</span></span>

### <span data-ttu-id="93966-131">System. String</span><span class="sxs-lookup"><span data-stu-id="93966-131">System.String</span></span>

### <span data-ttu-id="93966-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93966-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93966-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93966-133">OUTPUTS</span></span>

### <span data-ttu-id="93966-134">System. String</span><span class="sxs-lookup"><span data-stu-id="93966-134">System.String</span></span>

## <span data-ttu-id="93966-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="93966-135">NOTES</span></span>

## <span data-ttu-id="93966-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93966-136">RELATED LINKS</span></span>

[<span data-ttu-id="93966-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93966-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="93966-138">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="93966-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="93966-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93966-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="93966-140">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="93966-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


