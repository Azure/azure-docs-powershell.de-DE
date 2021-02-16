---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163025"
---
# <span data-ttu-id="2125b-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2125b-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="2125b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2125b-102">SYNOPSIS</span></span>
<span data-ttu-id="2125b-103">Listet die Speichertabellen auf.</span><span class="sxs-lookup"><span data-stu-id="2125b-103">Lists the storage tables.</span></span>

## <span data-ttu-id="2125b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2125b-104">SYNTAX</span></span>

### <span data-ttu-id="2125b-105">TableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2125b-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2125b-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="2125b-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2125b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2125b-107">DESCRIPTION</span></span>
<span data-ttu-id="2125b-108">Das **Cmdlet "Get-AzStorageTable"** listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2125b-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="2125b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2125b-109">EXAMPLES</span></span>

### <span data-ttu-id="2125b-110">Beispiel 1: Auflisten aller Azure Storage-Tabellen</span><span class="sxs-lookup"><span data-stu-id="2125b-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="2125b-111">Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="2125b-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="2125b-112">Beispiel 2: Auflisten von Azure Storage-Tabellen mit einem Platzhalterzeichen</span><span class="sxs-lookup"><span data-stu-id="2125b-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="2125b-113">Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen zu erhalten, deren Name mit der Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="2125b-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="2125b-114">Beispiel 3: Auflisten von Azure Storage-Tabellen mit dem Tabellennamenpräfix</span><span class="sxs-lookup"><span data-stu-id="2125b-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="2125b-115">Dieser Befehl verwendet den *Präfixparameter,* um Speichertabellen zu erhalten, deren Name mit der Tabelle beginnt.</span><span class="sxs-lookup"><span data-stu-id="2125b-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="2125b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2125b-116">PARAMETERS</span></span>

### <span data-ttu-id="2125b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="2125b-117">-Context</span></span>
<span data-ttu-id="2125b-118">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="2125b-118">Specifies the storage context.</span></span>
<span data-ttu-id="2125b-119">Zum Erstellen können Sie das cmdlet New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="2125b-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2125b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2125b-120">-DefaultProfile</span></span>
<span data-ttu-id="2125b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2125b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2125b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2125b-122">-Name</span></span>
<span data-ttu-id="2125b-123">Gibt den Tabellennamen an.</span><span class="sxs-lookup"><span data-stu-id="2125b-123">Specifies the table name.</span></span>
<span data-ttu-id="2125b-124">Wenn der Tabellenname leer ist, werden im Cmdlet alle Tabellen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2125b-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="2125b-125">Andernfalls werden alle Tabellen aufgeführt, die dem angegebenen Namen oder dem normalen Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2125b-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="2125b-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="2125b-126">-Prefix</span></span>
<span data-ttu-id="2125b-127">Gibt ein Präfix an, das im Namen der Tabelle oder Tabellen verwendet wird, die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="2125b-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="2125b-128">Auf diese Weise können Sie nach allen Tabellen suchen, die mit derselben Zeichenfolge beginnen, z. B. "Tabelle".</span><span class="sxs-lookup"><span data-stu-id="2125b-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="2125b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2125b-129">CommonParameters</span></span>
<span data-ttu-id="2125b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2125b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2125b-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2125b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2125b-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2125b-132">INPUTS</span></span>

### <span data-ttu-id="2125b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2125b-133">System.String</span></span>

### <span data-ttu-id="2125b-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2125b-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2125b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2125b-135">OUTPUTS</span></span>

### <span data-ttu-id="2125b-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2125b-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="2125b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2125b-137">NOTES</span></span>

## <span data-ttu-id="2125b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2125b-138">RELATED LINKS</span></span>

[<span data-ttu-id="2125b-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2125b-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="2125b-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2125b-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


