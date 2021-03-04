---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bb60e46f6785b29f8c2d64aadcce4d8697f4e16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938824"
---
# <span data-ttu-id="e7ad2-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7ad2-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e7ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ad2-103">Löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e7ad2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7ad2-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ad2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ad2-106">Das **Cmdlet Remove-AzDataLakeStoreAccount** löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e7ad2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="e7ad2-108">Beispiel 1: Entfernen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="e7ad2-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e7ad2-109">Mit diesem Befehl wird das Konto mit dem Namen ContosoADL aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="e7ad2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7ad2-110">PARAMETERS</span></span>

### <span data-ttu-id="e7ad2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ad2-111">-DefaultProfile</span></span>
<span data-ttu-id="e7ad2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e7ad2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7ad2-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e7ad2-113">-Force</span></span>
<span data-ttu-id="e7ad2-114">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e7ad2-115">-Name</span></span>
<span data-ttu-id="e7ad2-116">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="e7ad2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7ad2-117">-PassThru</span></span>
<span data-ttu-id="e7ad2-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7ad2-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ad2-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7ad2-121">Gibt die Ressourcengruppe an, die das zu entfernende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ad2-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7ad2-122">-Confirm</span></span>
<span data-ttu-id="e7ad2-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ad2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ad2-124">-WhatIf</span></span>
<span data-ttu-id="e7ad2-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ad2-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ad2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ad2-127">CommonParameters</span></span>
<span data-ttu-id="e7ad2-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ad2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ad2-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ad2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ad2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7ad2-130">INPUTS</span></span>

### <span data-ttu-id="e7ad2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e7ad2-131">System.String</span></span>

## <span data-ttu-id="e7ad2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7ad2-132">OUTPUTS</span></span>

### <span data-ttu-id="e7ad2-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7ad2-133">System.Boolean</span></span>

## <span data-ttu-id="e7ad2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7ad2-134">NOTES</span></span>

## <span data-ttu-id="e7ad2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7ad2-135">RELATED LINKS</span></span>

[<span data-ttu-id="e7ad2-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7ad2-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e7ad2-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7ad2-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e7ad2-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7ad2-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e7ad2-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7ad2-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


