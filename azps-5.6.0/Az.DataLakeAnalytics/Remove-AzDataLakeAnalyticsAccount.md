---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945184"
---
# <span data-ttu-id="ebfe6-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ebfe6-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ebfe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfe6-103">Löscht ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ebfe6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebfe6-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfe6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebfe6-105">DESCRIPTION</span></span>
<span data-ttu-id="ebfe6-106">Das **Cmdlet Remove-AzDataLakeAnalyticsAccount** löscht ein Azure Data Lake Analytics-Konto endgültig.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ebfe6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebfe6-107">EXAMPLES</span></span>

### <span data-ttu-id="ebfe6-108">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="ebfe6-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="ebfe6-109">Mit diesem Befehl wird das angegebene Data Lake Analytics-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="ebfe6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ebfe6-110">PARAMETERS</span></span>

### <span data-ttu-id="ebfe6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfe6-111">-DefaultProfile</span></span>
<span data-ttu-id="ebfe6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ebfe6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebfe6-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ebfe6-113">-Force</span></span>
<span data-ttu-id="ebfe6-114">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebfe6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ebfe6-115">-Name</span></span>
<span data-ttu-id="ebfe6-116">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ebfe6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebfe6-117">-PassThru</span></span>
<span data-ttu-id="ebfe6-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebfe6-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebfe6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfe6-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebfe6-121">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="ebfe6-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ebfe6-122">-Confirm</span></span>
<span data-ttu-id="ebfe6-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebfe6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfe6-124">-WhatIf</span></span>
<span data-ttu-id="ebfe6-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebfe6-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebfe6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfe6-127">CommonParameters</span></span>
<span data-ttu-id="ebfe6-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfe6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfe6-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfe6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfe6-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebfe6-130">INPUTS</span></span>

### <span data-ttu-id="ebfe6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ebfe6-131">System.String</span></span>

## <span data-ttu-id="ebfe6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebfe6-132">OUTPUTS</span></span>

### <span data-ttu-id="ebfe6-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebfe6-133">System.Boolean</span></span>

## <span data-ttu-id="ebfe6-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ebfe6-134">NOTES</span></span>

## <span data-ttu-id="ebfe6-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ebfe6-135">RELATED LINKS</span></span>

[<span data-ttu-id="ebfe6-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ebfe6-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ebfe6-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ebfe6-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ebfe6-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ebfe6-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ebfe6-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ebfe6-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


