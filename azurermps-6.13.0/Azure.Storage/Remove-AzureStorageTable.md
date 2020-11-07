---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: a4083920e935077658d218663e0a0255f6566ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663025"
---
# <span data-ttu-id="75bbb-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="75bbb-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="75bbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="75bbb-103">Entfernt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="75bbb-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75bbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75bbb-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75bbb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="75bbb-106">Das Cmdlet **Remove-AzureStorageTable** entfernt mindestens eine Speichertabelle aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="75bbb-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="75bbb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="75bbb-108">Beispiel 1: Entfernen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="75bbb-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="75bbb-109">Mit diesem Befehl wird eine Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="75bbb-109">This command removes a table.</span></span>

### <span data-ttu-id="75bbb-110">Beispiel 2: Entfernen mehrerer Tabellen</span><span class="sxs-lookup"><span data-stu-id="75bbb-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="75bbb-111">In diesem Beispiel wird ein Platzhalterzeichen mit dem *Name* -Parameter verwendet, um alle Tabellen abzurufen, die der Mustertabelle entsprechen, und übergibt dann das Ergebnis an die Pipeline, um die Tabellen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="75bbb-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="75bbb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75bbb-112">PARAMETERS</span></span>

### <span data-ttu-id="75bbb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="75bbb-113">-Context</span></span>
<span data-ttu-id="75bbb-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="75bbb-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="75bbb-115">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="75bbb-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="75bbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bbb-116">-DefaultProfile</span></span>
<span data-ttu-id="75bbb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75bbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75bbb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75bbb-118">-Force</span></span>
<span data-ttu-id="75bbb-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="75bbb-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="75bbb-120">-Name</span></span>
<span data-ttu-id="75bbb-121">Gibt den Namen der zu entfernenden Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="75bbb-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="75bbb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75bbb-122">-PassThru</span></span>
<span data-ttu-id="75bbb-123">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="75bbb-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="75bbb-124">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="75bbb-124">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75bbb-125">-Confirm</span></span>
<span data-ttu-id="75bbb-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75bbb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bbb-127">-WhatIf</span></span>
<span data-ttu-id="75bbb-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75bbb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75bbb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75bbb-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bbb-130">CommonParameters</span></span>
<span data-ttu-id="75bbb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75bbb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bbb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75bbb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bbb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75bbb-133">INPUTS</span></span>

### <span data-ttu-id="75bbb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="75bbb-134">System.String</span></span>

### <span data-ttu-id="75bbb-135">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="75bbb-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75bbb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75bbb-136">OUTPUTS</span></span>

### <span data-ttu-id="75bbb-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75bbb-137">System.Boolean</span></span>

## <span data-ttu-id="75bbb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="75bbb-138">NOTES</span></span>

## <span data-ttu-id="75bbb-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75bbb-139">RELATED LINKS</span></span>

[<span data-ttu-id="75bbb-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="75bbb-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
