---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162473"
---
# <span data-ttu-id="b95d3-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b95d3-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="b95d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b95d3-103">Löscht eine Anwendung aus einem Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="b95d3-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="b95d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b95d3-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b95d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b95d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b95d3-106">Das **Cmdlet "Remove-AzBatchApplication"** löscht eine Anwendung aus einem Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="b95d3-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="b95d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b95d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b95d3-108">Beispiel 1: Löschen einer Anwendung aus einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="b95d3-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="b95d3-109">Mit diesem Befehl wird die Anwendung Litware aus dem ContosoBatch-Konto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b95d3-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="b95d3-110">Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="b95d3-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="b95d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95d3-111">PARAMETERS</span></span>

### <span data-ttu-id="b95d3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b95d3-112">-AccountName</span></span>
<span data-ttu-id="b95d3-113">Gibt den Namen des Batchkontos an, aus dem dieses Cmdlet eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b95d3-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="b95d3-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b95d3-114">-ApplicationName</span></span>
<span data-ttu-id="b95d3-115">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b95d3-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="b95d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95d3-116">-DefaultProfile</span></span>
<span data-ttu-id="b95d3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95d3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="b95d3-119">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="b95d3-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b95d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95d3-120">CommonParameters</span></span>
<span data-ttu-id="b95d3-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95d3-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b95d3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95d3-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b95d3-123">INPUTS</span></span>

### <span data-ttu-id="b95d3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b95d3-124">System.String</span></span>

## <span data-ttu-id="b95d3-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b95d3-125">OUTPUTS</span></span>

### <span data-ttu-id="b95d3-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="b95d3-126">System.Void</span></span>

## <span data-ttu-id="b95d3-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b95d3-127">NOTES</span></span>

## <span data-ttu-id="b95d3-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b95d3-128">RELATED LINKS</span></span>

[<span data-ttu-id="b95d3-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b95d3-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="b95d3-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b95d3-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="b95d3-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b95d3-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="b95d3-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b95d3-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="b95d3-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b95d3-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="b95d3-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b95d3-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


