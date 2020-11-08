---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004890"
---
# <span data-ttu-id="6e982-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e982-101">New-AzStorageTable</span></span>

## <span data-ttu-id="6e982-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e982-102">SYNOPSIS</span></span>
<span data-ttu-id="6e982-103">Erstellt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="6e982-103">Creates a storage table.</span></span>

## <span data-ttu-id="6e982-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e982-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e982-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e982-105">DESCRIPTION</span></span>
<span data-ttu-id="6e982-106">Das Cmdlet **New-AzStorageTable** erstellt eine Speichertabelle, die dem Speicherkonto in Azure zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6e982-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="6e982-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e982-107">EXAMPLES</span></span>

### <span data-ttu-id="6e982-108">Beispiel 1: Erstellen einer Azure-Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="6e982-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="6e982-109">Dieser Befehl erstellt eine Speichertabelle mit dem Namen tableabc.</span><span class="sxs-lookup"><span data-stu-id="6e982-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="6e982-110">Beispiel 2: Erstellen mehrerer Azure-Speichertabellen</span><span class="sxs-lookup"><span data-stu-id="6e982-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="6e982-111">Dieser Befehl erstellt mehrere Tabellen.</span><span class="sxs-lookup"><span data-stu-id="6e982-111">This command creates multiple tables.</span></span>
<span data-ttu-id="6e982-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e982-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="6e982-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e982-113">PARAMETERS</span></span>

### <span data-ttu-id="6e982-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6e982-114">-Context</span></span>
<span data-ttu-id="6e982-115">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="6e982-115">Specifies the storage context.</span></span>
<span data-ttu-id="6e982-116">Sie können das New-AzStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e982-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e982-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e982-117">-DefaultProfile</span></span>
<span data-ttu-id="6e982-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e982-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e982-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6e982-119">-Name</span></span>
<span data-ttu-id="6e982-120">Gibt einen Namen für die neue Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="6e982-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e982-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e982-121">CommonParameters</span></span>
<span data-ttu-id="6e982-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e982-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e982-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e982-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e982-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e982-124">INPUTS</span></span>

### <span data-ttu-id="6e982-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6e982-125">System.String</span></span>

### <span data-ttu-id="6e982-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e982-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e982-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e982-127">OUTPUTS</span></span>

### <span data-ttu-id="6e982-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e982-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="6e982-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e982-129">NOTES</span></span>

## <span data-ttu-id="6e982-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e982-130">RELATED LINKS</span></span>

[<span data-ttu-id="6e982-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e982-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="6e982-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e982-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


