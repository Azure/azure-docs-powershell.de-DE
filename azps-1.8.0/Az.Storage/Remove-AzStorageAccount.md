---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: fadeb5c9fdee8028364f8e65ccd7e7e70a20572b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658791"
---
# <span data-ttu-id="9e2eb-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e2eb-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="9e2eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2eb-103">Entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="9e2eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e2eb-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e2eb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e2eb-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2eb-106">Das Cmdlet **Remove-AzStorageAccount** entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="9e2eb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e2eb-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2eb-108">Beispiel 1: Entfernen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9e2eb-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="9e2eb-109">Mit diesem Befehl wird das angegebene Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="9e2eb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e2eb-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e2eb-111">-AsJob</span></span>
<span data-ttu-id="9e2eb-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9e2eb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e2eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2eb-113">-DefaultProfile</span></span>
<span data-ttu-id="9e2eb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2eb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9e2eb-115">-Force</span></span>
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

### <span data-ttu-id="9e2eb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9e2eb-116">-Name</span></span>
<span data-ttu-id="9e2eb-117">Gibt den Namen des zu entfernenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e2eb-119">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2eb-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e2eb-120">-Confirm</span></span>
<span data-ttu-id="9e2eb-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2eb-122">-WhatIf</span></span>
<span data-ttu-id="9e2eb-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e2eb-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2eb-125">CommonParameters</span></span>
<span data-ttu-id="9e2eb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2eb-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2eb-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e2eb-128">INPUTS</span></span>

### <span data-ttu-id="9e2eb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2eb-129">System.String</span></span>

## <span data-ttu-id="9e2eb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e2eb-130">OUTPUTS</span></span>

### <span data-ttu-id="9e2eb-131">System. void</span><span class="sxs-lookup"><span data-stu-id="9e2eb-131">System.Void</span></span>

## <span data-ttu-id="9e2eb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e2eb-132">NOTES</span></span>

## <span data-ttu-id="9e2eb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e2eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="9e2eb-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e2eb-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="9e2eb-135">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e2eb-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="9e2eb-136">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e2eb-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


