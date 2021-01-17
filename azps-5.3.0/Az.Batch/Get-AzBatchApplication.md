---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471195"
---
# <span data-ttu-id="53a39-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a39-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="53a39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a39-102">SYNOPSIS</span></span>
<span data-ttu-id="53a39-103">Ruft Informationen zur angegebenen Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="53a39-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="53a39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53a39-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53a39-105">DESCRIPTION</span></span>
<span data-ttu-id="53a39-106">Das **Cmdlet "Get-AzBatchApplication"** ruft Informationen zu einer Anwendung in einem Azure -Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="53a39-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="53a39-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53a39-107">EXAMPLES</span></span>

### <span data-ttu-id="53a39-108">Beispiel 1: Anzeigen der Anwendungen in einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="53a39-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="53a39-109">Dieser Befehl zeigt alle Anwendungen im ContosoBatch-Konto an.</span><span class="sxs-lookup"><span data-stu-id="53a39-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="53a39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a39-110">PARAMETERS</span></span>

### <span data-ttu-id="53a39-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="53a39-111">-AccountName</span></span>
<span data-ttu-id="53a39-112">Gibt den Namen des Batchkontos an, das die Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="53a39-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="53a39-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="53a39-113">-ApplicationName</span></span>
<span data-ttu-id="53a39-114">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="53a39-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a39-115">-DefaultProfile</span></span>
<span data-ttu-id="53a39-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53a39-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a39-117">-ResourceGroupName</span></span>
<span data-ttu-id="53a39-118">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="53a39-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="53a39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a39-119">CommonParameters</span></span>
<span data-ttu-id="53a39-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a39-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a39-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a39-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53a39-122">INPUTS</span></span>

### <span data-ttu-id="53a39-123">System.String</span><span class="sxs-lookup"><span data-stu-id="53a39-123">System.String</span></span>

## <span data-ttu-id="53a39-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53a39-124">OUTPUTS</span></span>

### <span data-ttu-id="53a39-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="53a39-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="53a39-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53a39-126">NOTES</span></span>

## <span data-ttu-id="53a39-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53a39-127">RELATED LINKS</span></span>

[<span data-ttu-id="53a39-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a39-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="53a39-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a39-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="53a39-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a39-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="53a39-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a39-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="53a39-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a39-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="53a39-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a39-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


