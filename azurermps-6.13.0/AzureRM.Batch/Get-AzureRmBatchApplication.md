---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: 2a1096d4424ff920c84c8fe7a2a4704496f95dfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477969"
---
# <span data-ttu-id="099f2-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="099f2-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="099f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="099f2-102">SYNOPSIS</span></span>
<span data-ttu-id="099f2-103">Ruft Informationen zur angegebenen Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="099f2-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="099f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="099f2-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="099f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="099f2-105">DESCRIPTION</span></span>
<span data-ttu-id="099f2-106">Das Cmdlet " **Get-AzureRmBatchApplication** " Ruft Informationen zu einer Anwendung in einem Azure-Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="099f2-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="099f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="099f2-107">EXAMPLES</span></span>

### <span data-ttu-id="099f2-108">Beispiel 1: Anzeigen der Anwendungen in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="099f2-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="099f2-109">Dieser Befehl zeigt alle Anwendungen im ContosoBatch-Konto an.</span><span class="sxs-lookup"><span data-stu-id="099f2-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="099f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="099f2-110">PARAMETERS</span></span>

### <span data-ttu-id="099f2-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="099f2-111">-AccountName</span></span>
<span data-ttu-id="099f2-112">Gibt den Namen des Batch Kontos an, das die Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="099f2-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="099f2-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="099f2-113">-ApplicationId</span></span>
<span data-ttu-id="099f2-114">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="099f2-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="099f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099f2-115">-DefaultProfile</span></span>
<span data-ttu-id="099f2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="099f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="099f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="099f2-118">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="099f2-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="099f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099f2-119">CommonParameters</span></span>
<span data-ttu-id="099f2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099f2-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099f2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099f2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="099f2-122">INPUTS</span></span>

### <span data-ttu-id="099f2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="099f2-123">System.String</span></span>

## <span data-ttu-id="099f2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="099f2-124">OUTPUTS</span></span>

### <span data-ttu-id="099f2-125">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="099f2-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="099f2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="099f2-126">NOTES</span></span>

## <span data-ttu-id="099f2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="099f2-127">RELATED LINKS</span></span>

[<span data-ttu-id="099f2-128">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="099f2-128">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="099f2-129">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="099f2-129">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="099f2-130">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="099f2-130">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="099f2-131">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="099f2-131">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="099f2-132">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="099f2-132">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="099f2-133">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="099f2-133">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


