---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 013d53649cc579ae305ab738e6d2bd1138646a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480018"
---
# <span data-ttu-id="3b59d-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3b59d-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="3b59d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b59d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b59d-103">Entfernt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="3b59d-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b59d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b59d-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b59d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b59d-105">DESCRIPTION</span></span>
<span data-ttu-id="3b59d-106">Das Cmdlet **Remove-AzureStorageTable** entfernt mindestens eine Speichertabelle aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59d-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="3b59d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b59d-107">EXAMPLES</span></span>

### <span data-ttu-id="3b59d-108">Beispiel 1: Entfernen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="3b59d-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="3b59d-109">Mit diesem Befehl wird eine Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b59d-109">This command removes a table.</span></span>

### <span data-ttu-id="3b59d-110">Beispiel 2: Entfernen mehrerer Tabellen</span><span class="sxs-lookup"><span data-stu-id="3b59d-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="3b59d-111">In diesem Beispiel wird ein Platzhalterzeichen mit dem *Name* -Parameter verwendet, um alle Tabellen abzurufen, die der Mustertabelle entsprechen, und übergibt dann das Ergebnis an die Pipeline, um die Tabellen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3b59d-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="3b59d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b59d-112">PARAMETERS</span></span>

### <span data-ttu-id="3b59d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3b59d-113">-Context</span></span>
<span data-ttu-id="3b59d-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="3b59d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3b59d-115">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b59d-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3b59d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3b59d-116">-Force</span></span>
<span data-ttu-id="3b59d-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3b59d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b59d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3b59d-118">-Name</span></span>
<span data-ttu-id="3b59d-119">Gibt den Namen der zu entfernenden Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="3b59d-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="3b59d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b59d-120">-PassThru</span></span>
<span data-ttu-id="3b59d-121">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="3b59d-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3b59d-122">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3b59d-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b59d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b59d-123">-Confirm</span></span>
<span data-ttu-id="3b59d-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b59d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b59d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b59d-125">-WhatIf</span></span>
<span data-ttu-id="3b59d-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b59d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b59d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b59d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b59d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b59d-128">CommonParameters</span></span>
<span data-ttu-id="3b59d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b59d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b59d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b59d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b59d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b59d-131">INPUTS</span></span>

### <span data-ttu-id="3b59d-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b59d-132">IStorageContext</span></span>

<span data-ttu-id="3b59d-133">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b59d-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3b59d-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3b59d-134">String</span></span>

<span data-ttu-id="3b59d-135">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b59d-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3b59d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b59d-136">OUTPUTS</span></span>

### <span data-ttu-id="3b59d-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b59d-137">System.Boolean</span></span>

## <span data-ttu-id="3b59d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b59d-138">NOTES</span></span>

## <span data-ttu-id="3b59d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b59d-139">RELATED LINKS</span></span>

[<span data-ttu-id="3b59d-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3b59d-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
