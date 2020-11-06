---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475646"
---
# <span data-ttu-id="5952f-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5952f-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="5952f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5952f-102">SYNOPSIS</span></span>
<span data-ttu-id="5952f-103">Listet die Speichertabellen auf.</span><span class="sxs-lookup"><span data-stu-id="5952f-103">Lists the storage tables.</span></span>

## <span data-ttu-id="5952f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5952f-104">SYNTAX</span></span>

### <span data-ttu-id="5952f-105">Tabellenname (Standard)</span><span class="sxs-lookup"><span data-stu-id="5952f-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5952f-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="5952f-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5952f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5952f-107">DESCRIPTION</span></span>
<span data-ttu-id="5952f-108">Das Cmdlet " **Get-AzureStorageTable** " listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5952f-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="5952f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5952f-109">EXAMPLES</span></span>

### <span data-ttu-id="5952f-110">Beispiel 1: Auflisten aller Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="5952f-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="5952f-111">Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="5952f-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="5952f-112">Beispiel 2: Auflisten von Azure-Speichertabellen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="5952f-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="5952f-113">Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="5952f-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="5952f-114">Beispiel 3: Auflisten von Azure-Speichertabellen mit dem Tabellennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="5952f-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="5952f-115">Dieser Befehl verwendet den *prefix* -Parameter, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="5952f-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="5952f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5952f-116">PARAMETERS</span></span>

### <span data-ttu-id="5952f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="5952f-117">-Context</span></span>
<span data-ttu-id="5952f-118">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5952f-118">Specifies the storage context.</span></span>
<span data-ttu-id="5952f-119">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5952f-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5952f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5952f-120">-Name</span></span>
<span data-ttu-id="5952f-121">Gibt den Tabellennamen an.</span><span class="sxs-lookup"><span data-stu-id="5952f-121">Specifies the table name.</span></span>
<span data-ttu-id="5952f-122">Wenn der Tabellenname leer ist, listet das Cmdlet alle Tabellen auf.</span><span class="sxs-lookup"><span data-stu-id="5952f-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="5952f-123">Andernfalls werden alle Tabellen aufgelistet, die dem angegebenen Namen oder dem Muster des regulären namens entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5952f-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5952f-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5952f-124">-Prefix</span></span>
<span data-ttu-id="5952f-125">Gibt ein Präfix an, das für den Namen der Tabelle oder der Tabellen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="5952f-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="5952f-126">Sie können damit alle Tabellen suchen, die mit der gleichen Zeichenfolge beginnen, beispielsweise Table.</span><span class="sxs-lookup"><span data-stu-id="5952f-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5952f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5952f-127">CommonParameters</span></span>
<span data-ttu-id="5952f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5952f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5952f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5952f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5952f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5952f-130">INPUTS</span></span>

## <span data-ttu-id="5952f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5952f-131">OUTPUTS</span></span>

## <span data-ttu-id="5952f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5952f-132">NOTES</span></span>

## <span data-ttu-id="5952f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5952f-133">RELATED LINKS</span></span>

[<span data-ttu-id="5952f-134">Neu – AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5952f-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="5952f-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5952f-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


