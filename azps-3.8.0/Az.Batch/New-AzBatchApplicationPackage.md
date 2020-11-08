---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997147"
---
# <span data-ttu-id="655e5-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="655e5-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="655e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="655e5-102">SYNOPSIS</span></span>
<span data-ttu-id="655e5-103">Erstellt ein Anwendungspaket in einem Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="655e5-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="655e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="655e5-104">SYNTAX</span></span>

### <span data-ttu-id="655e5-105">UploadAndActivate (Standard)</span><span class="sxs-lookup"><span data-stu-id="655e5-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="655e5-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="655e5-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="655e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="655e5-107">DESCRIPTION</span></span>
<span data-ttu-id="655e5-108">Mit dem Cmdlet **New-AzBatchApplicationPackage** wird ein Anwendungspaket in einem Azure-Batch Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="655e5-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="655e5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="655e5-109">EXAMPLES</span></span>

### <span data-ttu-id="655e5-110">Beispiel 1: Installieren eines Anwendungspakets in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="655e5-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="655e5-111">Mit diesem Befehl wird Version 1,0 der Litware-Anwendung erstellt und aktiviert, und der Inhalt von litware.1.0.zip wird als Inhalt des Anwendungspakets hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="655e5-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="655e5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="655e5-112">PARAMETERS</span></span>

### <span data-ttu-id="655e5-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="655e5-113">-AccountName</span></span>
<span data-ttu-id="655e5-114">Gibt den Namen des Batch Kontos an, dem dieses Cmdlet ein Anwendungspaket hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="655e5-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="655e5-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="655e5-115">-ActivateOnly</span></span>
<span data-ttu-id="655e5-116">Gibt an, dass dieses Cmdlet ein Anwendungspaket aktiviert, das bereits hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="655e5-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="655e5-117">-ApplicationName</span></span>
<span data-ttu-id="655e5-118">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="655e5-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="655e5-119">-ApplicationVersion</span></span>
<span data-ttu-id="655e5-120">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="655e5-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655e5-121">-DefaultProfile</span></span>
<span data-ttu-id="655e5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="655e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="655e5-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="655e5-123">-FilePath</span></span>
<span data-ttu-id="655e5-124">Gibt die Datei an, die als Binärdatei des Anwendungspakets hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="655e5-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-125">-Format</span><span class="sxs-lookup"><span data-stu-id="655e5-125">-Format</span></span>
<span data-ttu-id="655e5-126">Gibt das Format der Binärdatei des Anwendungspakets an.</span><span class="sxs-lookup"><span data-stu-id="655e5-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="655e5-128">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="655e5-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655e5-129">CommonParameters</span></span>
<span data-ttu-id="655e5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="655e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655e5-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="655e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655e5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="655e5-132">INPUTS</span></span>

### <span data-ttu-id="655e5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="655e5-133">System.String</span></span>

### <span data-ttu-id="655e5-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="655e5-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="655e5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="655e5-135">OUTPUTS</span></span>

### <span data-ttu-id="655e5-136">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="655e5-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="655e5-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="655e5-137">NOTES</span></span>

## <span data-ttu-id="655e5-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="655e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="655e5-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="655e5-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="655e5-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="655e5-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="655e5-141">Neu – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="655e5-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="655e5-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="655e5-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="655e5-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="655e5-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="655e5-144">Satz-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="655e5-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


