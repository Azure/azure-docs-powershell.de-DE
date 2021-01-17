---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472550"
---
# <span data-ttu-id="6bd88-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bd88-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="6bd88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd88-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd88-103">Entfernt eine Datenquelle aus einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="6bd88-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6bd88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bd88-104">SYNTAX</span></span>

### <span data-ttu-id="6bd88-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bd88-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bd88-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bd88-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd88-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bd88-107">DESCRIPTION</span></span>
<span data-ttu-id="6bd88-108">Das **Cmdlet "Remove-AzDataLakeAnalyticsDataSource"** entfernt eine Datenquelle aus einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="6bd88-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6bd88-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bd88-109">EXAMPLES</span></span>

### <span data-ttu-id="6bd88-110">Beispiel 1: Entfernen einer Datenquelle</span><span class="sxs-lookup"><span data-stu-id="6bd88-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="6bd88-111">Mit diesem Befehl wird die Datenquelle mit dem Namen "AzureStorage01" aus dem Konto "ContosoAdlAccount" entfernt.</span><span class="sxs-lookup"><span data-stu-id="6bd88-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="6bd88-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bd88-112">PARAMETERS</span></span>

### <span data-ttu-id="6bd88-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="6bd88-113">-Account</span></span>
<span data-ttu-id="6bd88-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6bd88-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6bd88-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6bd88-115">-Blob</span></span>
<span data-ttu-id="6bd88-116">Gibt den Namen des zu entfernenden AzureBlob -Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="6bd88-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd88-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd88-117">-DataLakeStore</span></span>
<span data-ttu-id="6bd88-118">Gibt den Namen des zu entfernenden AzureData Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6bd88-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd88-119">-DefaultProfile</span></span>
<span data-ttu-id="6bd88-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6bd88-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bd88-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6bd88-121">-Force</span></span>
<span data-ttu-id="6bd88-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="6bd88-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bd88-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bd88-123">-PassThru</span></span>
<span data-ttu-id="6bd88-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6bd88-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6bd88-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6bd88-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6bd88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd88-126">-ResourceGroupName</span></span>
<span data-ttu-id="6bd88-127">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6bd88-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd88-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bd88-128">-Confirm</span></span>
<span data-ttu-id="6bd88-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bd88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd88-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6bd88-130">-WhatIf</span></span>
<span data-ttu-id="6bd88-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bd88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd88-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bd88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd88-133">CommonParameters</span></span>
<span data-ttu-id="6bd88-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd88-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd88-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd88-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bd88-136">INPUTS</span></span>

### <span data-ttu-id="6bd88-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6bd88-137">System.String</span></span>

## <span data-ttu-id="6bd88-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bd88-138">OUTPUTS</span></span>

### <span data-ttu-id="6bd88-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bd88-139">System.Boolean</span></span>

## <span data-ttu-id="6bd88-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6bd88-140">NOTES</span></span>

## <span data-ttu-id="6bd88-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6bd88-141">RELATED LINKS</span></span>

[<span data-ttu-id="6bd88-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bd88-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6bd88-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bd88-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


