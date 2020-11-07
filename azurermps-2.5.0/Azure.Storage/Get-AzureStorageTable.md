---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 834400893dc3d2065a8ca3f0b27783e0a4d5604e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849844"
---
# <span data-ttu-id="34646-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="34646-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="34646-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34646-102">SYNOPSIS</span></span>
<span data-ttu-id="34646-103">Listet die Speichertabellen auf.</span><span class="sxs-lookup"><span data-stu-id="34646-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34646-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34646-104">SYNTAX</span></span>

### <span data-ttu-id="34646-105">Tabellenname (Standard)</span><span class="sxs-lookup"><span data-stu-id="34646-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34646-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="34646-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34646-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34646-107">DESCRIPTION</span></span>
<span data-ttu-id="34646-108">Das Cmdlet " **Get-AzureStorageTable** " listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34646-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="34646-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34646-109">EXAMPLES</span></span>

### <span data-ttu-id="34646-110">Beispiel 1: Auflisten aller Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="34646-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="34646-111">Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="34646-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="34646-112">Beispiel 2: Auflisten von Azure-Speichertabellen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="34646-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="34646-113">Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="34646-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="34646-114">Beispiel 3: Auflisten von Azure-Speichertabellen mit dem Tabellennamen Präfix</span><span class="sxs-lookup"><span data-stu-id="34646-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="34646-115">Dieser Befehl verwendet den *prefix* -Parameter, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="34646-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="34646-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="34646-116">PARAMETERS</span></span>

### <span data-ttu-id="34646-117">-Context</span><span class="sxs-lookup"><span data-stu-id="34646-117">-Context</span></span>
<span data-ttu-id="34646-118">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="34646-118">Specifies the storage context.</span></span>
<span data-ttu-id="34646-119">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34646-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34646-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34646-120">-DefaultProfile</span></span>
<span data-ttu-id="34646-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34646-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34646-122">-Name</span><span class="sxs-lookup"><span data-stu-id="34646-122">-Name</span></span>
<span data-ttu-id="34646-123">Gibt den Tabellennamen an.</span><span class="sxs-lookup"><span data-stu-id="34646-123">Specifies the table name.</span></span>
<span data-ttu-id="34646-124">Wenn der Tabellenname leer ist, listet das Cmdlet alle Tabellen auf.</span><span class="sxs-lookup"><span data-stu-id="34646-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="34646-125">Andernfalls werden alle Tabellen aufgelistet, die dem angegebenen Namen oder dem Muster des regulären namens entsprechen.</span><span class="sxs-lookup"><span data-stu-id="34646-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34646-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="34646-126">-Prefix</span></span>
<span data-ttu-id="34646-127">Gibt ein Präfix an, das für den Namen der Tabelle oder der Tabellen verwendet wird, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="34646-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="34646-128">Sie können damit alle Tabellen suchen, die mit der gleichen Zeichenfolge beginnen, beispielsweise Table.</span><span class="sxs-lookup"><span data-stu-id="34646-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34646-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34646-129">CommonParameters</span></span>
<span data-ttu-id="34646-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34646-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34646-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34646-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34646-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34646-132">INPUTS</span></span>

### <span data-ttu-id="34646-133">System. String</span><span class="sxs-lookup"><span data-stu-id="34646-133">System.String</span></span>

### <span data-ttu-id="34646-134">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34646-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34646-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34646-135">OUTPUTS</span></span>

### <span data-ttu-id="34646-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="34646-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="34646-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="34646-137">NOTES</span></span>

## <span data-ttu-id="34646-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34646-138">RELATED LINKS</span></span>

[<span data-ttu-id="34646-139">Neu – AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="34646-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="34646-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="34646-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


