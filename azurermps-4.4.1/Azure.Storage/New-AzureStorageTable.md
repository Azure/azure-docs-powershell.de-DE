---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 2f051fb0724ac266753d87fc30489398a4aa64a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480045"
---
# <span data-ttu-id="aecfe-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aecfe-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="aecfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aecfe-102">SYNOPSIS</span></span>
<span data-ttu-id="aecfe-103">Erstellt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="aecfe-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aecfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aecfe-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="aecfe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aecfe-105">DESCRIPTION</span></span>
<span data-ttu-id="aecfe-106">Das Cmdlet **New-AzureStorageTable** erstellt eine Speichertabelle, die dem Speicherkonto in Azure zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aecfe-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="aecfe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aecfe-107">EXAMPLES</span></span>

### <span data-ttu-id="aecfe-108">Beispiel 1: Erstellen einer Azure-Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="aecfe-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="aecfe-109">Dieser Befehl erstellt eine Speichertabelle mit dem Namen tableabc.</span><span class="sxs-lookup"><span data-stu-id="aecfe-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="aecfe-110">Beispiel 2: Erstellen mehrerer Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="aecfe-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="aecfe-111">Dieser Befehl erstellt mehrere Tabellen.</span><span class="sxs-lookup"><span data-stu-id="aecfe-111">This command creates multiple tables.</span></span>
<span data-ttu-id="aecfe-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="aecfe-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="aecfe-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="aecfe-113">PARAMETERS</span></span>

### <span data-ttu-id="aecfe-114">-Context</span><span class="sxs-lookup"><span data-stu-id="aecfe-114">-Context</span></span>
<span data-ttu-id="aecfe-115">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="aecfe-115">Specifies the storage context.</span></span>
<span data-ttu-id="aecfe-116">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aecfe-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aecfe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aecfe-117">-Name</span></span>
<span data-ttu-id="aecfe-118">Gibt einen Namen für die neue Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="aecfe-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aecfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecfe-119">CommonParameters</span></span>
<span data-ttu-id="aecfe-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aecfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecfe-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecfe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecfe-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aecfe-122">INPUTS</span></span>

### <span data-ttu-id="aecfe-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aecfe-123">IStorageContext</span></span>

<span data-ttu-id="aecfe-124">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="aecfe-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="aecfe-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="aecfe-125">String</span></span>

<span data-ttu-id="aecfe-126">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="aecfe-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="aecfe-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aecfe-127">OUTPUTS</span></span>

### <span data-ttu-id="aecfe-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aecfe-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="aecfe-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="aecfe-129">NOTES</span></span>

## <span data-ttu-id="aecfe-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aecfe-130">RELATED LINKS</span></span>

[<span data-ttu-id="aecfe-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aecfe-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="aecfe-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="aecfe-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


