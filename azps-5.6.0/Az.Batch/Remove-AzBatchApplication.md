---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: ebe28df5c69ce966a9d05d2e34cd9e66693d7f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939699"
---
# <span data-ttu-id="97773-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="97773-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="97773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97773-102">SYNOPSIS</span></span>
<span data-ttu-id="97773-103">Löscht eine Anwendung aus einem Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="97773-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="97773-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97773-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97773-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97773-105">DESCRIPTION</span></span>
<span data-ttu-id="97773-106">Das **Cmdlet Remove-AzBatchApplication** löscht eine Anwendung aus einem Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="97773-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="97773-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97773-107">EXAMPLES</span></span>

### <span data-ttu-id="97773-108">Beispiel 1: Löschen einer Anwendung aus einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="97773-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="97773-109">Mit diesem Befehl wird die Litware-Anwendung aus dem ContosoBatch-Konto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="97773-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="97773-110">Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="97773-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="97773-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="97773-111">PARAMETERS</span></span>

### <span data-ttu-id="97773-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97773-112">-AccountName</span></span>
<span data-ttu-id="97773-113">Gibt den Namen des Batchkontos an, aus dem dieses Cmdlet eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="97773-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="97773-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="97773-114">-ApplicationName</span></span>
<span data-ttu-id="97773-115">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="97773-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="97773-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97773-116">-DefaultProfile</span></span>
<span data-ttu-id="97773-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97773-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97773-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97773-118">-ResourceGroupName</span></span>
<span data-ttu-id="97773-119">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="97773-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="97773-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97773-120">CommonParameters</span></span>
<span data-ttu-id="97773-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97773-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97773-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97773-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97773-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97773-123">INPUTS</span></span>

### <span data-ttu-id="97773-124">System.String</span><span class="sxs-lookup"><span data-stu-id="97773-124">System.String</span></span>

## <span data-ttu-id="97773-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97773-125">OUTPUTS</span></span>

### <span data-ttu-id="97773-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="97773-126">System.Void</span></span>

## <span data-ttu-id="97773-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="97773-127">NOTES</span></span>

## <span data-ttu-id="97773-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="97773-128">RELATED LINKS</span></span>

[<span data-ttu-id="97773-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="97773-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="97773-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="97773-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="97773-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="97773-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="97773-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="97773-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="97773-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="97773-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="97773-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="97773-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


