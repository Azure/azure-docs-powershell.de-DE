---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475645"
---
# <span data-ttu-id="02492-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02492-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="02492-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02492-102">SYNOPSIS</span></span>
<span data-ttu-id="02492-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="02492-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="02492-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02492-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="02492-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02492-105">DESCRIPTION</span></span>
<span data-ttu-id="02492-106">Das Cmdlet " **Get-AzureStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="02492-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="02492-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02492-107">EXAMPLES</span></span>

### <span data-ttu-id="02492-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="02492-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="02492-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="02492-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="02492-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="02492-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="02492-111">Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="02492-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="02492-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02492-112">PARAMETERS</span></span>

### <span data-ttu-id="02492-113">-Context</span><span class="sxs-lookup"><span data-stu-id="02492-113">-Context</span></span>
<span data-ttu-id="02492-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="02492-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="02492-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02492-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="02492-116">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="02492-116">-Policy</span></span>
<span data-ttu-id="02492-117">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="02492-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="02492-118">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="02492-118">-Table</span></span>
<span data-ttu-id="02492-119">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="02492-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="02492-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02492-120">CommonParameters</span></span>
<span data-ttu-id="02492-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02492-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02492-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02492-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02492-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02492-123">INPUTS</span></span>

## <span data-ttu-id="02492-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02492-124">OUTPUTS</span></span>

## <span data-ttu-id="02492-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="02492-125">NOTES</span></span>

## <span data-ttu-id="02492-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02492-126">RELATED LINKS</span></span>

[<span data-ttu-id="02492-127">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02492-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="02492-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02492-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="02492-129">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02492-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="02492-130">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="02492-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


