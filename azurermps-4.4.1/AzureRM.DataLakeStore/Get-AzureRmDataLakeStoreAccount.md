---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479249"
---
# <span data-ttu-id="ebbcb-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="ebbcb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebbcb-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbcb-103">Ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebbcb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebbcb-104">SYNTAX</span></span>

### <span data-ttu-id="ebbcb-105">Alle im Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="ebbcb-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebbcb-106">Alle in der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ebbcb-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebbcb-107">Bestimmtes Konto</span><span class="sxs-lookup"><span data-stu-id="ebbcb-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebbcb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebbcb-108">DESCRIPTION</span></span>
<span data-ttu-id="ebbcb-109">Das Cmdlet " **Get-AzureRmDataLakeStoreAccount** " ruft Details zu einem Data Lake Store-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="ebbcb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebbcb-110">EXAMPLES</span></span>

### <span data-ttu-id="ebbcb-111">Beispiel 1: Abrufen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="ebbcb-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="ebbcb-112">Dieser Befehl ruft das Konto mit dem Namen ContosoADL ab.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="ebbcb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebbcb-113">PARAMETERS</span></span>

### <span data-ttu-id="ebbcb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ebbcb-114">-Name</span></span>
<span data-ttu-id="ebbcb-115">Gibt den Namen des abzurufenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbcb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbcb-116">-ResourceGroupName</span></span>
<span data-ttu-id="ebbcb-117">Gibt den Namen der Ressourcengruppe an, die das abzurufende Data Lake Store-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbcb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbcb-118">-DefaultProfile</span></span>
<span data-ttu-id="ebbcb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebbcb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbcb-120">CommonParameters</span></span>
<span data-ttu-id="ebbcb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbcb-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbcb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbcb-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebbcb-123">INPUTS</span></span>

## <span data-ttu-id="ebbcb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebbcb-124">OUTPUTS</span></span>

### <span data-ttu-id="ebbcb-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="ebbcb-126">Das spezifische Data Lake Store-Konto, nach dem gefragt wurde.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="ebbcb-127">Liste<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="ebbcb-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="ebbcb-128">Eine Liste der Data Lake Store-Konten in der Ressourcengruppe oder dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebbcb-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="ebbcb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebbcb-129">NOTES</span></span>

## <span data-ttu-id="ebbcb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebbcb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebbcb-131">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ebbcb-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ebbcb-133">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ebbcb-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ebbcb-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


