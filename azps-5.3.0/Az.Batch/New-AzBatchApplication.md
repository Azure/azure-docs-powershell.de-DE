---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471148"
---
# <span data-ttu-id="ce511-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ce511-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="ce511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce511-102">SYNOPSIS</span></span>
<span data-ttu-id="ce511-103">Fügt dem angegebenen Batchkonto eine Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce511-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="ce511-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce511-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce511-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce511-105">DESCRIPTION</span></span>
<span data-ttu-id="ce511-106">Das **Cmdlet "New-AzBatchApplication"** fügt dem angegebenen Azure -Batchkonto eine Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce511-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="ce511-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce511-107">EXAMPLES</span></span>

### <span data-ttu-id="ce511-108">Beispiel 1: Hinzufügen einer leeren Anwendung zu einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="ce511-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="ce511-109">Mit diesem Befehl wird die Anwendung Litware im ContosoBatch-Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce511-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="ce511-110">Die Anwendung enthält zunächst keine Pakete.</span><span class="sxs-lookup"><span data-stu-id="ce511-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="ce511-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce511-111">PARAMETERS</span></span>

### <span data-ttu-id="ce511-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ce511-112">-AccountName</span></span>
<span data-ttu-id="ce511-113">Gibt den Namen des Batchkontos an, dem dieses Cmdlet eine Anwendung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ce511-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="ce511-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="ce511-114">-AllowUpdates</span></span>
<span data-ttu-id="ce511-115">Gibt an, ob Pakete innerhalb der Anwendung mit derselben Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="ce511-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce511-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce511-116">-ApplicationName</span></span>
<span data-ttu-id="ce511-117">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ce511-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="ce511-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce511-118">-DefaultProfile</span></span>
<span data-ttu-id="ce511-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce511-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce511-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ce511-120">-DisplayName</span></span>
<span data-ttu-id="ce511-121">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ce511-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="ce511-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce511-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce511-123">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="ce511-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ce511-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce511-124">CommonParameters</span></span>
<span data-ttu-id="ce511-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce511-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce511-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce511-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce511-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce511-127">INPUTS</span></span>

### <span data-ttu-id="ce511-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ce511-128">System.String</span></span>

### <span data-ttu-id="ce511-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ce511-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ce511-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce511-130">OUTPUTS</span></span>

### <span data-ttu-id="ce511-131">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ce511-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="ce511-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce511-132">NOTES</span></span>

## <span data-ttu-id="ce511-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce511-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce511-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ce511-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="ce511-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ce511-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="ce511-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ce511-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ce511-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ce511-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ce511-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ce511-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="ce511-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ce511-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


