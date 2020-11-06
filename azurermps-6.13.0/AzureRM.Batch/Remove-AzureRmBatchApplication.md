---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 61288340bb2b9acb2bd47388d8f776d5c732b6f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477945"
---
# <span data-ttu-id="a09ce-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a09ce-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a09ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a09ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a09ce-103">Löscht eine Anwendung aus einem Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="a09ce-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a09ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a09ce-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a09ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a09ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a09ce-106">Das Cmdlet **Remove-AzureRmBatchApplication** löscht eine Anwendung aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="a09ce-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="a09ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a09ce-107">EXAMPLES</span></span>

### <span data-ttu-id="a09ce-108">Beispiel 1: Löschen einer Anwendung aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="a09ce-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="a09ce-109">Dieser Befehl löscht die Litware-Anwendung aus dem ContosoBatch-Konto.</span><span class="sxs-lookup"><span data-stu-id="a09ce-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="a09ce-110">Der Befehl schlägt fehl, wenn die Anwendung Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="a09ce-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="a09ce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a09ce-111">PARAMETERS</span></span>

### <span data-ttu-id="a09ce-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a09ce-112">-AccountName</span></span>
<span data-ttu-id="a09ce-113">Gibt den Namen des Batch Kontos an, aus dem dieses Cmdlet eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="a09ce-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="a09ce-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a09ce-114">-ApplicationId</span></span>
<span data-ttu-id="a09ce-115">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="a09ce-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09ce-116">-DefaultProfile</span></span>
<span data-ttu-id="a09ce-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a09ce-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a09ce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09ce-118">-ResourceGroupName</span></span>
<span data-ttu-id="a09ce-119">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="a09ce-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a09ce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09ce-120">CommonParameters</span></span>
<span data-ttu-id="a09ce-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09ce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09ce-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09ce-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09ce-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a09ce-123">INPUTS</span></span>

### <span data-ttu-id="a09ce-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a09ce-124">System.String</span></span>

## <span data-ttu-id="a09ce-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a09ce-125">OUTPUTS</span></span>

### <span data-ttu-id="a09ce-126">System. void</span><span class="sxs-lookup"><span data-stu-id="a09ce-126">System.Void</span></span>

## <span data-ttu-id="a09ce-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a09ce-127">NOTES</span></span>

## <span data-ttu-id="a09ce-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a09ce-128">RELATED LINKS</span></span>

[<span data-ttu-id="a09ce-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a09ce-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a09ce-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a09ce-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a09ce-131">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a09ce-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="a09ce-132">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a09ce-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a09ce-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a09ce-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a09ce-134">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a09ce-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


