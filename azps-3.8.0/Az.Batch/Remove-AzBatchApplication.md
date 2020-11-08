---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997137"
---
# <span data-ttu-id="74166-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74166-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="74166-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74166-102">SYNOPSIS</span></span>
<span data-ttu-id="74166-103">Löscht eine Anwendung aus einem Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="74166-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="74166-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74166-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74166-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74166-105">DESCRIPTION</span></span>
<span data-ttu-id="74166-106">Das Cmdlet **Remove-AzBatchApplication** löscht eine Anwendung aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="74166-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="74166-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74166-107">EXAMPLES</span></span>

### <span data-ttu-id="74166-108">Beispiel 1: Löschen einer Anwendung aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="74166-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="74166-109">Dieser Befehl löscht die Litware-Anwendung aus dem ContosoBatch-Konto.</span><span class="sxs-lookup"><span data-stu-id="74166-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="74166-110">Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="74166-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="74166-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="74166-111">PARAMETERS</span></span>

### <span data-ttu-id="74166-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="74166-112">-AccountName</span></span>
<span data-ttu-id="74166-113">Gibt den Namen des Batch Kontos an, aus dem dieses Cmdlet eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="74166-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="74166-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="74166-114">-ApplicationName</span></span>
<span data-ttu-id="74166-115">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="74166-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="74166-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74166-116">-DefaultProfile</span></span>
<span data-ttu-id="74166-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74166-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74166-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74166-118">-ResourceGroupName</span></span>
<span data-ttu-id="74166-119">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="74166-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="74166-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74166-120">CommonParameters</span></span>
<span data-ttu-id="74166-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74166-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74166-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74166-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74166-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74166-123">INPUTS</span></span>

### <span data-ttu-id="74166-124">System. String</span><span class="sxs-lookup"><span data-stu-id="74166-124">System.String</span></span>

## <span data-ttu-id="74166-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74166-125">OUTPUTS</span></span>

### <span data-ttu-id="74166-126">System. void</span><span class="sxs-lookup"><span data-stu-id="74166-126">System.Void</span></span>

## <span data-ttu-id="74166-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="74166-127">NOTES</span></span>

## <span data-ttu-id="74166-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74166-128">RELATED LINKS</span></span>

[<span data-ttu-id="74166-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74166-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="74166-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74166-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="74166-131">Neu – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74166-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="74166-132">Neu – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74166-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="74166-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74166-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="74166-134">Satz-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74166-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


