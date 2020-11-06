---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496713"
---
# <span data-ttu-id="53b0e-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53b0e-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="53b0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="53b0e-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="53b0e-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53b0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b0e-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="53b0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="53b0e-106">Das Cmdlet **New-AzureStorageTableStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="53b0e-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="53b0e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53b0e-107">EXAMPLES</span></span>

### <span data-ttu-id="53b0e-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="53b0e-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="53b0e-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy02 in der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="53b0e-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="53b0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b0e-110">PARAMETERS</span></span>

### <span data-ttu-id="53b0e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="53b0e-111">-Context</span></span>
<span data-ttu-id="53b0e-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="53b0e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53b0e-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53b0e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53b0e-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="53b0e-114">-ExpiryTime</span></span>
<span data-ttu-id="53b0e-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="53b0e-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b0e-116">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="53b0e-116">-Permission</span></span>
<span data-ttu-id="53b0e-117">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speichertabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="53b0e-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="53b0e-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="53b0e-118">-Policy</span></span>
<span data-ttu-id="53b0e-119">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="53b0e-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b0e-120">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="53b0e-120">-StartTime</span></span>
<span data-ttu-id="53b0e-121">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="53b0e-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b0e-122">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="53b0e-122">-Table</span></span>
<span data-ttu-id="53b0e-123">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="53b0e-123">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53b0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b0e-124">CommonParameters</span></span>
<span data-ttu-id="53b0e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b0e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b0e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53b0e-127">INPUTS</span></span>

### <span data-ttu-id="53b0e-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53b0e-128">IStorageContext</span></span>

<span data-ttu-id="53b0e-129">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="53b0e-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="53b0e-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="53b0e-130">String</span></span>

<span data-ttu-id="53b0e-131">Der Parameter "Tabelle" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="53b0e-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="53b0e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53b0e-132">OUTPUTS</span></span>

### <span data-ttu-id="53b0e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="53b0e-133">System.String</span></span>

## <span data-ttu-id="53b0e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="53b0e-134">NOTES</span></span>

## <span data-ttu-id="53b0e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53b0e-135">RELATED LINKS</span></span>

[<span data-ttu-id="53b0e-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53b0e-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="53b0e-137">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="53b0e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="53b0e-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53b0e-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="53b0e-139">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53b0e-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


