---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458094"
---
# <span data-ttu-id="6ef28-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="6ef28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef28-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef28-103">Ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6ef28-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6ef28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ef28-104">SYNTAX</span></span>

### <span data-ttu-id="6ef28-105">GetAllInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ef28-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ef28-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ef28-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ef28-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ef28-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ef28-108">DESCRIPTION</span></span>
<span data-ttu-id="6ef28-109">Das **Cmdlet "Get-AzDataLakeStoreAccount"** ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6ef28-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6ef28-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ef28-110">EXAMPLES</span></span>

### <span data-ttu-id="6ef28-111">Beispiel 1: Erhalten eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="6ef28-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6ef28-112">Dieser Befehl ruft das Konto mit dem Namen "ContosoADL" ab.</span><span class="sxs-lookup"><span data-stu-id="6ef28-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="6ef28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ef28-113">PARAMETERS</span></span>

### <span data-ttu-id="6ef28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef28-114">-DefaultProfile</span></span>
<span data-ttu-id="6ef28-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6ef28-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ef28-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6ef28-116">-Name</span></span>
<span data-ttu-id="6ef28-117">Gibt den Namen des zu erhaltenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6ef28-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef28-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ef28-119">Gibt den Namen der Ressourcengruppe an, die das zu erhaltende Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="6ef28-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef28-120">CommonParameters</span></span>
<span data-ttu-id="6ef28-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef28-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef28-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef28-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef28-123">INPUTS</span></span>

### <span data-ttu-id="6ef28-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6ef28-124">System.String</span></span>

## <span data-ttu-id="6ef28-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef28-125">OUTPUTS</span></span>

### <span data-ttu-id="6ef28-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="6ef28-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ef28-127">NOTES</span></span>

## <span data-ttu-id="6ef28-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ef28-128">RELATED LINKS</span></span>

[<span data-ttu-id="6ef28-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6ef28-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6ef28-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="6ef28-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ef28-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


