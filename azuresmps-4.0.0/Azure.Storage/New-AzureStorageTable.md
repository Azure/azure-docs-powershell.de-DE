---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475497"
---
# <span data-ttu-id="d48f1-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d48f1-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="d48f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d48f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d48f1-103">Erstellt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="d48f1-103">Creates a storage table.</span></span>

## <span data-ttu-id="d48f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48f1-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d48f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d48f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d48f1-106">Das Cmdlet **New-AzureStorageTable** erstellt eine Speichertabelle, die dem Speicherkonto in Azure zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d48f1-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d48f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d48f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d48f1-108">Beispiel 1: Erstellen einer Azure-Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="d48f1-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="d48f1-109">Dieser Befehl erstellt eine Speichertabelle mit dem Namen tableabc.</span><span class="sxs-lookup"><span data-stu-id="d48f1-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="d48f1-110">Beispiel 2: Erstellen mehrerer Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="d48f1-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="d48f1-111">Dieser Befehl erstellt mehrere Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d48f1-111">This command creates multiple tables.</span></span>
<span data-ttu-id="d48f1-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d48f1-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d48f1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d48f1-113">PARAMETERS</span></span>

### <span data-ttu-id="d48f1-114">-Context</span><span class="sxs-lookup"><span data-stu-id="d48f1-114">-Context</span></span>
<span data-ttu-id="d48f1-115">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d48f1-115">Specifies the storage context.</span></span>
<span data-ttu-id="d48f1-116">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d48f1-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d48f1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d48f1-117">-Name</span></span>
<span data-ttu-id="d48f1-118">Gibt einen Namen für die neue Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="d48f1-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="d48f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48f1-119">CommonParameters</span></span>
<span data-ttu-id="d48f1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48f1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48f1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48f1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d48f1-122">INPUTS</span></span>

## <span data-ttu-id="d48f1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d48f1-123">OUTPUTS</span></span>

## <span data-ttu-id="d48f1-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d48f1-124">NOTES</span></span>

## <span data-ttu-id="d48f1-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d48f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="d48f1-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d48f1-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="d48f1-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d48f1-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


