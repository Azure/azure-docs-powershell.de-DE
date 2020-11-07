---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: d564b9a0bf2f35240b1de75e2531858876a17475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663513"
---
# <span data-ttu-id="fd0a1-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd0a1-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fd0a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0a1-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd0a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd0a1-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd0a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd0a1-105">DESCRIPTION</span></span>
<span data-ttu-id="fd0a1-106">Das Cmdlet " **Get-AzureStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="fd0a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd0a1-107">EXAMPLES</span></span>

### <span data-ttu-id="fd0a1-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="fd0a1-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="fd0a1-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="fd0a1-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="fd0a1-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="fd0a1-111">Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="fd0a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd0a1-112">PARAMETERS</span></span>

### <span data-ttu-id="fd0a1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="fd0a1-113">-Context</span></span>
<span data-ttu-id="fd0a1-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fd0a1-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd0a1-116">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fd0a1-116">-Policy</span></span>
<span data-ttu-id="fd0a1-117">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd0a1-118">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="fd0a1-118">-Table</span></span>
<span data-ttu-id="fd0a1-119">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="fd0a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0a1-120">CommonParameters</span></span>
<span data-ttu-id="fd0a1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0a1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd0a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0a1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd0a1-123">INPUTS</span></span>

### <span data-ttu-id="fd0a1-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd0a1-124">IStorageContext</span></span>

<span data-ttu-id="fd0a1-125">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fd0a1-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fd0a1-126">String</span></span>

<span data-ttu-id="fd0a1-127">Der Parameter "Tabelle" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fd0a1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd0a1-128">OUTPUTS</span></span>

### <span data-ttu-id="fd0a1-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="fd0a1-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="fd0a1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd0a1-130">NOTES</span></span>

## <span data-ttu-id="fd0a1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd0a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd0a1-132">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd0a1-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fd0a1-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd0a1-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fd0a1-134">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd0a1-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fd0a1-135">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd0a1-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


