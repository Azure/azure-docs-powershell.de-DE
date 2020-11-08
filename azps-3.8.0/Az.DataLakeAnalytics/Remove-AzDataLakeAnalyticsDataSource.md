---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995242"
---
# <span data-ttu-id="1c2ae-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c2ae-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1c2ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2ae-103">Entfernt eine Datenquelle aus einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1c2ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c2ae-104">SYNTAX</span></span>

### <span data-ttu-id="1c2ae-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c2ae-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c2ae-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c2ae-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c2ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c2ae-107">DESCRIPTION</span></span>
<span data-ttu-id="1c2ae-108">Das Cmdlet **Remove-AzDataLakeAnalyticsDataSource** entfernt eine Datenquelle aus einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1c2ae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c2ae-109">EXAMPLES</span></span>

### <span data-ttu-id="1c2ae-110">Beispiel 1: Entfernen einer Datenquelle</span><span class="sxs-lookup"><span data-stu-id="1c2ae-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="1c2ae-111">Dieser Befehl entfernt die Datenquelle mit dem Namen AzureStorage01 aus dem Konto mit dem Namen ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="1c2ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c2ae-112">PARAMETERS</span></span>

### <span data-ttu-id="1c2ae-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="1c2ae-113">-Account</span></span>
<span data-ttu-id="1c2ae-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1c2ae-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1c2ae-115">-Blob</span></span>
<span data-ttu-id="1c2ae-116">Gibt den Namen des zu entfernenden AzureBlob-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="1c2ae-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c2ae-117">-DataLakeStore</span></span>
<span data-ttu-id="1c2ae-118">Gibt den Namen des AzureData Lake Store-Kontos an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="1c2ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2ae-119">-DefaultProfile</span></span>
<span data-ttu-id="1c2ae-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1c2ae-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c2ae-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1c2ae-121">-Force</span></span>
<span data-ttu-id="1c2ae-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c2ae-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c2ae-123">-PassThru</span></span>
<span data-ttu-id="1c2ae-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c2ae-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c2ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c2ae-127">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1c2ae-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c2ae-128">-Confirm</span></span>
<span data-ttu-id="1c2ae-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2ae-130">-WhatIf</span></span>
<span data-ttu-id="1c2ae-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c2ae-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2ae-133">CommonParameters</span></span>
<span data-ttu-id="1c2ae-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2ae-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2ae-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2ae-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c2ae-136">INPUTS</span></span>

### <span data-ttu-id="1c2ae-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1c2ae-137">System.String</span></span>

## <span data-ttu-id="1c2ae-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c2ae-138">OUTPUTS</span></span>

### <span data-ttu-id="1c2ae-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c2ae-139">System.Boolean</span></span>

## <span data-ttu-id="1c2ae-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c2ae-140">NOTES</span></span>

## <span data-ttu-id="1c2ae-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c2ae-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c2ae-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c2ae-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1c2ae-143">Satz-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c2ae-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


