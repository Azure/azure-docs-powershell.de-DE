---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 621aa03b2819815dc538650ea30120c63009235e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503094"
---
# <span data-ttu-id="73352-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73352-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="73352-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73352-102">SYNOPSIS</span></span>
<span data-ttu-id="73352-103">Erstellt ein Anwendungspaket in einem Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="73352-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73352-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73352-104">SYNTAX</span></span>

### <span data-ttu-id="73352-105">UploadAndActivate (Standard)</span><span class="sxs-lookup"><span data-stu-id="73352-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73352-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="73352-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73352-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73352-107">DESCRIPTION</span></span>
<span data-ttu-id="73352-108">Mit dem Cmdlet **New-AzureRmBatchApplicationPackage** wird ein Anwendungspaket in einem Azure-Batch Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="73352-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="73352-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73352-109">EXAMPLES</span></span>

### <span data-ttu-id="73352-110">Beispiel 1: Installieren eines Anwendungspakets in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="73352-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="73352-111">Mit diesem Befehl wird Version 1,0 der Litware-Anwendung erstellt und aktiviert, und der Inhalt von litware.1.0.zip wird als Inhalt des Anwendungspakets hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="73352-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="73352-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="73352-112">PARAMETERS</span></span>

### <span data-ttu-id="73352-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="73352-113">-AccountName</span></span>
<span data-ttu-id="73352-114">Gibt den Namen des Batch Kontos an, dem dieses Cmdlet ein Anwendungspaket hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="73352-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="73352-115">-ActivateOnly</span></span>
<span data-ttu-id="73352-116">Gibt an, dass dieses Cmdlet ein Anwendungspaket aktiviert, das bereits hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="73352-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="73352-117">-ApplicationId</span></span>
<span data-ttu-id="73352-118">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="73352-118">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="73352-119">-ApplicationVersion</span></span>
<span data-ttu-id="73352-120">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="73352-120">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73352-121">-DefaultProfile</span></span>
<span data-ttu-id="73352-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73352-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73352-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="73352-123">-FilePath</span></span>
<span data-ttu-id="73352-124">Gibt die Datei an, die als Binärdatei des Anwendungspakets hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="73352-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-125">-Format</span><span class="sxs-lookup"><span data-stu-id="73352-125">-Format</span></span>
<span data-ttu-id="73352-126">Gibt das Format der Binärdatei des Anwendungspakets an.</span><span class="sxs-lookup"><span data-stu-id="73352-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73352-127">-ResourceGroupName</span></span>
<span data-ttu-id="73352-128">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="73352-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73352-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73352-129">CommonParameters</span></span>
<span data-ttu-id="73352-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73352-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73352-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73352-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73352-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73352-132">INPUTS</span></span>

### <span data-ttu-id="73352-133">Keine</span><span class="sxs-lookup"><span data-stu-id="73352-133">None</span></span>
<span data-ttu-id="73352-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="73352-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73352-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73352-135">OUTPUTS</span></span>

### <span data-ttu-id="73352-136">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73352-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="73352-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="73352-137">NOTES</span></span>

## <span data-ttu-id="73352-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73352-138">RELATED LINKS</span></span>

[<span data-ttu-id="73352-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73352-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="73352-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73352-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="73352-141">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73352-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="73352-142">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73352-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="73352-143">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73352-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="73352-144">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73352-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


