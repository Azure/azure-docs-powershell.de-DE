---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: 7c51776683d4a8ecb777fd56d8b83ca4ae672206
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927459"
---
# <span data-ttu-id="849fa-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="849fa-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="849fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="849fa-102">SYNOPSIS</span></span>
<span data-ttu-id="849fa-103">Löscht einen Anwendungspaketdatensatz und die Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="849fa-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="849fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="849fa-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="849fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="849fa-105">DESCRIPTION</span></span>
<span data-ttu-id="849fa-106">Das **Cmdlet Remove-AzBatchApplicationPackage** löscht einen Anwendungspaketdatensatz und die Binärdatei aus einem Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="849fa-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="849fa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="849fa-107">EXAMPLES</span></span>

### <span data-ttu-id="849fa-108">Beispiel 1: Löschen eines Anwendungspakets aus einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="849fa-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="849fa-109">Mit diesem Befehl wird Version 1.0 der Litware-Anwendung aus dem ContosoBatchGroup-Konto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="849fa-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="849fa-110">Der Befehl löscht sowohl den Paketdatensatz als auch den Blob, der die Paket binäre Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="849fa-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="849fa-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="849fa-111">PARAMETERS</span></span>

### <span data-ttu-id="849fa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="849fa-112">-AccountName</span></span>
<span data-ttu-id="849fa-113">Gibt den Namen des Batchkontos an, aus dem dieses Cmdlet ein Anwendungspaket löscht.</span><span class="sxs-lookup"><span data-stu-id="849fa-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="849fa-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="849fa-114">-ApplicationName</span></span>
<span data-ttu-id="849fa-115">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="849fa-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="849fa-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="849fa-116">-ApplicationVersion</span></span>
<span data-ttu-id="849fa-117">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="849fa-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="849fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849fa-118">-DefaultProfile</span></span>
<span data-ttu-id="849fa-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="849fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="849fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="849fa-121">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="849fa-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="849fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849fa-122">CommonParameters</span></span>
<span data-ttu-id="849fa-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849fa-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="849fa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849fa-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="849fa-125">INPUTS</span></span>

### <span data-ttu-id="849fa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="849fa-126">System.String</span></span>

## <span data-ttu-id="849fa-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="849fa-127">OUTPUTS</span></span>

### <span data-ttu-id="849fa-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="849fa-128">System.Void</span></span>

## <span data-ttu-id="849fa-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="849fa-129">NOTES</span></span>

## <span data-ttu-id="849fa-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="849fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="849fa-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="849fa-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="849fa-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="849fa-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="849fa-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="849fa-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="849fa-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="849fa-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="849fa-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="849fa-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="849fa-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="849fa-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


