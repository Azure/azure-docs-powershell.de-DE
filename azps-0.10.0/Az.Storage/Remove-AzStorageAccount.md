---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: d969dcc0906def107b68a76980b39482dfe8c4e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842948"
---
# <span data-ttu-id="d4179-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4179-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="d4179-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4179-102">SYNOPSIS</span></span>
<span data-ttu-id="d4179-103">Entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="d4179-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d4179-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4179-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4179-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4179-105">DESCRIPTION</span></span>
<span data-ttu-id="d4179-106">Das Cmdlet **Remove-AzStorageAccount** entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="d4179-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d4179-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4179-107">EXAMPLES</span></span>

### <span data-ttu-id="d4179-108">Beispiel 1: Entfernen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d4179-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d4179-109">Mit diesem Befehl wird das angegebene Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4179-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="d4179-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4179-110">PARAMETERS</span></span>

### <span data-ttu-id="d4179-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4179-111">-AsJob</span></span>
<span data-ttu-id="d4179-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4179-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4179-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4179-113">-DefaultProfile</span></span>
<span data-ttu-id="d4179-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4179-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4179-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d4179-115">-Force</span></span>
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

### <span data-ttu-id="d4179-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d4179-116">-Name</span></span>
<span data-ttu-id="d4179-117">Gibt den Namen des zu entfernenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d4179-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="d4179-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4179-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4179-119">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="d4179-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="d4179-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4179-120">-Confirm</span></span>
<span data-ttu-id="d4179-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4179-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4179-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4179-122">-WhatIf</span></span>
<span data-ttu-id="d4179-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4179-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4179-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4179-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4179-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4179-125">CommonParameters</span></span>
<span data-ttu-id="d4179-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4179-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4179-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4179-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4179-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4179-128">INPUTS</span></span>

### <span data-ttu-id="d4179-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d4179-129">System.String</span></span>

## <span data-ttu-id="d4179-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4179-130">OUTPUTS</span></span>

### <span data-ttu-id="d4179-131">System. void</span><span class="sxs-lookup"><span data-stu-id="d4179-131">System.Void</span></span>

## <span data-ttu-id="d4179-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4179-132">NOTES</span></span>

## <span data-ttu-id="d4179-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4179-133">RELATED LINKS</span></span>

[<span data-ttu-id="d4179-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4179-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d4179-135">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4179-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d4179-136">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4179-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


