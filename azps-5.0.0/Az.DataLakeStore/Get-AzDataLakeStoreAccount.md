---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297897"
---
# <span data-ttu-id="b1e61-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="b1e61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1e61-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e61-103">Ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b1e61-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="b1e61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1e61-104">SYNTAX</span></span>

### <span data-ttu-id="b1e61-105">GetAllInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1e61-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1e61-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1e61-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1e61-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1e61-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1e61-108">DESCRIPTION</span></span>
<span data-ttu-id="b1e61-109">Das Cmdlet " **Get-AzDataLakeStoreAccount** " ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b1e61-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="b1e61-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1e61-110">EXAMPLES</span></span>

### <span data-ttu-id="b1e61-111">Beispiel 1: Abrufen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="b1e61-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="b1e61-112">Dieser Befehl ruft das Konto mit dem Namen ContosoADL ab.</span><span class="sxs-lookup"><span data-stu-id="b1e61-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="b1e61-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1e61-113">PARAMETERS</span></span>

### <span data-ttu-id="b1e61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e61-114">-DefaultProfile</span></span>
<span data-ttu-id="b1e61-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1e61-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1e61-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b1e61-116">-Name</span></span>
<span data-ttu-id="b1e61-117">Gibt den Namen des abzurufenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b1e61-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="b1e61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e61-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1e61-119">Gibt den Namen der Ressourcengruppe an, die das abzurufende Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="b1e61-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="b1e61-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e61-120">CommonParameters</span></span>
<span data-ttu-id="b1e61-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1e61-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e61-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e61-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e61-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1e61-123">INPUTS</span></span>

### <span data-ttu-id="b1e61-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b1e61-124">System.String</span></span>

## <span data-ttu-id="b1e61-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1e61-125">OUTPUTS</span></span>

### <span data-ttu-id="b1e61-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="b1e61-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1e61-127">NOTES</span></span>

## <span data-ttu-id="b1e61-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1e61-128">RELATED LINKS</span></span>

[<span data-ttu-id="b1e61-129">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b1e61-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b1e61-131">Satz-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b1e61-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b1e61-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


