---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300648"
---
# <span data-ttu-id="99b53-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="99b53-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="99b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b53-102">SYNOPSIS</span></span>
<span data-ttu-id="99b53-103">Die ACL einer Datei oder eines Ordners im Data Lake Store wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="99b53-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="99b53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99b53-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99b53-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99b53-105">DESCRIPTION</span></span>
<span data-ttu-id="99b53-106">Das **Cmdlet "Remove-AzDataLakeStoreItemAcl"** löscht die Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="99b53-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="99b53-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99b53-107">EXAMPLES</span></span>

### <span data-ttu-id="99b53-108">Beispiel 1: Entfernen der ACL aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="99b53-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="99b53-109">Mit diesem Befehl wird die ACL für das Stammverzeichnis für das Konto ContosoADL entfernt.</span><span class="sxs-lookup"><span data-stu-id="99b53-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="99b53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99b53-110">PARAMETERS</span></span>

### <span data-ttu-id="99b53-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="99b53-111">-Account</span></span>
<span data-ttu-id="99b53-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="99b53-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-113">-Default</span><span class="sxs-lookup"><span data-stu-id="99b53-113">-Default</span></span>
<span data-ttu-id="99b53-114">Gibt an, dass das Cmdlet die Standard-ACL für eine Datei oder einen Ordner entfernt.</span><span class="sxs-lookup"><span data-stu-id="99b53-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b53-115">-DefaultProfile</span></span>
<span data-ttu-id="99b53-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99b53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99b53-117">-Force</span></span>
<span data-ttu-id="99b53-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="99b53-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99b53-119">-PassThru</span></span>
<span data-ttu-id="99b53-120">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="99b53-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-121">-Path</span><span class="sxs-lookup"><span data-stu-id="99b53-121">-Path</span></span>
<span data-ttu-id="99b53-122">Gibt den Data Lake Store-Pfad des Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="99b53-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b53-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99b53-123">-Confirm</span></span>
<span data-ttu-id="99b53-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99b53-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b53-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="99b53-125">-WhatIf</span></span>
<span data-ttu-id="99b53-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99b53-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b53-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99b53-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b53-128">CommonParameters</span></span>
<span data-ttu-id="99b53-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b53-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b53-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b53-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99b53-131">INPUTS</span></span>

### <span data-ttu-id="99b53-132">System.String</span><span class="sxs-lookup"><span data-stu-id="99b53-132">System.String</span></span>

### <span data-ttu-id="99b53-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="99b53-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="99b53-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99b53-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99b53-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99b53-135">OUTPUTS</span></span>

### <span data-ttu-id="99b53-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99b53-136">System.Boolean</span></span>

## <span data-ttu-id="99b53-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99b53-137">NOTES</span></span>
* <span data-ttu-id="99b53-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="99b53-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="99b53-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99b53-139">RELATED LINKS</span></span>

[<span data-ttu-id="99b53-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="99b53-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="99b53-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="99b53-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="99b53-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="99b53-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


