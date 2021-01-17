---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458131"
---
# <span data-ttu-id="e05ee-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e05ee-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e05ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e05ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e05ee-103">Löscht ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="e05ee-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e05ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e05ee-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05ee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e05ee-105">DESCRIPTION</span></span>
<span data-ttu-id="e05ee-106">Das **Cmdlet "Remove-AzDataLakeAnalyticsAccount"** löscht ein Azure Data Lake Analytics-Konto endgültig.</span><span class="sxs-lookup"><span data-stu-id="e05ee-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e05ee-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e05ee-107">EXAMPLES</span></span>

### <span data-ttu-id="e05ee-108">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="e05ee-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e05ee-109">Mit diesem Befehl wird das angegebene Data Lake Analytics-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="e05ee-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="e05ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e05ee-110">PARAMETERS</span></span>

### <span data-ttu-id="e05ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05ee-111">-DefaultProfile</span></span>
<span data-ttu-id="e05ee-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e05ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e05ee-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e05ee-113">-Force</span></span>
<span data-ttu-id="e05ee-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="e05ee-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e05ee-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e05ee-115">-Name</span></span>
<span data-ttu-id="e05ee-116">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e05ee-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e05ee-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05ee-117">-PassThru</span></span>
<span data-ttu-id="e05ee-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e05ee-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e05ee-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e05ee-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e05ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="e05ee-121">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e05ee-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e05ee-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e05ee-122">-Confirm</span></span>
<span data-ttu-id="e05ee-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e05ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05ee-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e05ee-124">-WhatIf</span></span>
<span data-ttu-id="e05ee-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e05ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05ee-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e05ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05ee-127">CommonParameters</span></span>
<span data-ttu-id="e05ee-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05ee-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05ee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05ee-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e05ee-130">INPUTS</span></span>

### <span data-ttu-id="e05ee-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e05ee-131">System.String</span></span>

## <span data-ttu-id="e05ee-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e05ee-132">OUTPUTS</span></span>

### <span data-ttu-id="e05ee-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e05ee-133">System.Boolean</span></span>

## <span data-ttu-id="e05ee-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e05ee-134">NOTES</span></span>

## <span data-ttu-id="e05ee-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e05ee-135">RELATED LINKS</span></span>

[<span data-ttu-id="e05ee-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e05ee-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e05ee-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e05ee-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e05ee-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e05ee-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e05ee-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e05ee-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


