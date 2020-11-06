---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 5e0be2a9c9ba56fecee9e7c1e7ae37a3e39be110
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482553"
---
# <span data-ttu-id="6d145-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6d145-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="6d145-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d145-102">SYNOPSIS</span></span>
<span data-ttu-id="6d145-103">Ruft Informationen zu einem Anwendungspaket in einem Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6d145-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d145-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d145-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d145-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d145-105">DESCRIPTION</span></span>
<span data-ttu-id="6d145-106">Das Cmdlet " **Get-AzureRmBatchApplicationPackage** " Ruft Informationen zu einem Anwendungspaket in einem Azure-Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6d145-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="6d145-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d145-107">EXAMPLES</span></span>

### <span data-ttu-id="6d145-108">Beispiel 1: Abrufen von Details zu einem Anwendungspaket in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="6d145-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="6d145-109">Dieser Befehl ruft die Details der Version 1,0 des Litware-Pakets ab.</span><span class="sxs-lookup"><span data-stu-id="6d145-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="6d145-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d145-110">PARAMETERS</span></span>

### <span data-ttu-id="6d145-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6d145-111">-AccountName</span></span>
<span data-ttu-id="6d145-112">Gibt den Namen des Batch Kontos an, von dem dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="6d145-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="6d145-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6d145-113">-ApplicationId</span></span>
<span data-ttu-id="6d145-114">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="6d145-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="6d145-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="6d145-115">-ApplicationVersion</span></span>
<span data-ttu-id="6d145-116">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="6d145-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="6d145-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d145-117">-DefaultProfile</span></span>
<span data-ttu-id="6d145-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d145-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d145-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d145-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d145-120">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="6d145-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="6d145-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d145-121">CommonParameters</span></span>
<span data-ttu-id="6d145-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d145-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d145-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d145-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d145-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d145-124">INPUTS</span></span>

### <span data-ttu-id="6d145-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6d145-125">System.String</span></span>

## <span data-ttu-id="6d145-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d145-126">OUTPUTS</span></span>

### <span data-ttu-id="6d145-127">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6d145-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="6d145-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d145-128">NOTES</span></span>

## <span data-ttu-id="6d145-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d145-129">RELATED LINKS</span></span>

[<span data-ttu-id="6d145-130">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6d145-130">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="6d145-131">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6d145-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="6d145-132">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6d145-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="6d145-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6d145-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="6d145-134">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6d145-134">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="6d145-135">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6d145-135">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


