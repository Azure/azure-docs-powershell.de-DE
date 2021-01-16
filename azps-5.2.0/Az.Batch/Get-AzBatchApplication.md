---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299595"
---
# <span data-ttu-id="b9817-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b9817-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="b9817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9817-102">SYNOPSIS</span></span>
<span data-ttu-id="b9817-103">Ruft Informationen zur angegebenen Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="b9817-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="b9817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9817-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9817-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9817-105">DESCRIPTION</span></span>
<span data-ttu-id="b9817-106">Das **Cmdlet "Get-AzBatchApplication"** ruft Informationen zu einer Anwendung in einem Azure -Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="b9817-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="b9817-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9817-107">EXAMPLES</span></span>

### <span data-ttu-id="b9817-108">Beispiel 1: Anzeigen der Anwendungen in einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="b9817-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="b9817-109">Dieser Befehl zeigt alle Anwendungen im ContosoBatch-Konto an.</span><span class="sxs-lookup"><span data-stu-id="b9817-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="b9817-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9817-110">PARAMETERS</span></span>

### <span data-ttu-id="b9817-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9817-111">-AccountName</span></span>
<span data-ttu-id="b9817-112">Gibt den Namen des Batchkontos an, das die Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="b9817-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="b9817-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b9817-113">-ApplicationName</span></span>
<span data-ttu-id="b9817-114">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b9817-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="b9817-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9817-115">-DefaultProfile</span></span>
<span data-ttu-id="b9817-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9817-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9817-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9817-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9817-118">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="b9817-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b9817-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9817-119">CommonParameters</span></span>
<span data-ttu-id="b9817-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9817-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9817-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9817-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9817-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9817-122">INPUTS</span></span>

### <span data-ttu-id="b9817-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b9817-123">System.String</span></span>

## <span data-ttu-id="b9817-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9817-124">OUTPUTS</span></span>

### <span data-ttu-id="b9817-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="b9817-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="b9817-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9817-126">NOTES</span></span>

## <span data-ttu-id="b9817-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9817-127">RELATED LINKS</span></span>

[<span data-ttu-id="b9817-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b9817-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="b9817-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b9817-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="b9817-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b9817-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="b9817-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b9817-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="b9817-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b9817-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="b9817-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b9817-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


