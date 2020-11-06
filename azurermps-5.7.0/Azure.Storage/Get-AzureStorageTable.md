---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: ac25103ed8a933af4e118087371511842044b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496745"
---
# <span data-ttu-id="a2cd7-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a2cd7-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="a2cd7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a2cd7-103">Listet die Speichertabellen auf.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2cd7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2cd7-104">SYNTAX</span></span>

### <span data-ttu-id="a2cd7-105">Tabellenname (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2cd7-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="a2cd7-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="a2cd7-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a2cd7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2cd7-107">DESCRIPTION</span></span>
<span data-ttu-id="a2cd7-108">Das Cmdlet " **Get-AzureStorageTable** " listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a2cd7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2cd7-109">EXAMPLES</span></span>

### <span data-ttu-id="a2cd7-110">Beispiel 1: Auflisten aller Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="a2cd7-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="a2cd7-111">Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="a2cd7-112">Beispiel 2: Auflisten von Azure-Speichertabellen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="a2cd7-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="a2cd7-113">Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="a2cd7-114">Beispiel 3: Auflisten von Azure-Speichertabellen mit dem Tabellennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="a2cd7-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="a2cd7-115">Dieser Befehl verwendet den *prefix* -Parameter, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="a2cd7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2cd7-116">PARAMETERS</span></span>

### <span data-ttu-id="a2cd7-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a2cd7-117">-Context</span></span>
<span data-ttu-id="a2cd7-118">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-118">Specifies the storage context.</span></span>
<span data-ttu-id="a2cd7-119">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a2cd7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a2cd7-120">-Name</span></span>
<span data-ttu-id="a2cd7-121">Gibt den Tabellennamen an.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-121">Specifies the table name.</span></span>
<span data-ttu-id="a2cd7-122">Wenn der Tabellenname leer ist, listet das Cmdlet alle Tabellen auf.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="a2cd7-123">Andernfalls werden alle Tabellen aufgelistet, die dem angegebenen Namen oder dem Muster des regulären namens entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="a2cd7-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a2cd7-124">-Prefix</span></span>
<span data-ttu-id="a2cd7-125">Gibt ein Präfix an, das für den Namen der Tabelle oder der Tabellen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="a2cd7-126">Sie können damit alle Tabellen suchen, die mit der gleichen Zeichenfolge beginnen, beispielsweise Table.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="a2cd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2cd7-127">CommonParameters</span></span>
<span data-ttu-id="a2cd7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2cd7-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2cd7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2cd7-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2cd7-130">INPUTS</span></span>

### <span data-ttu-id="a2cd7-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2cd7-131">IStorageContext</span></span>

<span data-ttu-id="a2cd7-132">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a2cd7-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a2cd7-133">String</span></span>

<span data-ttu-id="a2cd7-134">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2cd7-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a2cd7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2cd7-135">OUTPUTS</span></span>

### <span data-ttu-id="a2cd7-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a2cd7-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="a2cd7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2cd7-137">NOTES</span></span>

## <span data-ttu-id="a2cd7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2cd7-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2cd7-139">Neu – AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a2cd7-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="a2cd7-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a2cd7-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


