---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: bce5110a4aa03686b8ae38ee03ea853bc6c89949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940416"
---
# <span data-ttu-id="a8398-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="a8398-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="a8398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8398-102">SYNOPSIS</span></span>
<span data-ttu-id="a8398-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="a8398-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="a8398-104">Diese Schlüssel sind der Authentifizierungsmechanismus, der bei nachfolgenden Aufrufen von Azure Maps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8398-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="a8398-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8398-105">SYNTAX</span></span>

### <span data-ttu-id="a8398-106">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8398-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8398-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8398-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8398-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8398-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8398-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8398-109">DESCRIPTION</span></span>
<span data-ttu-id="a8398-110">Das Get-AzMapsAccountKey-Cmdlet ruft die API-Schlüssel für ein bereitgestelltes Azure Maps-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="a8398-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="a8398-111">Ein Azure Maps-Konto verfügt über zwei API-Schlüssel: Primär und Sekundär.</span><span class="sxs-lookup"><span data-stu-id="a8398-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="a8398-112">Die Schlüssel ermöglichen die Interaktion mit dem Azure Maps-Kontoendpunkt.</span><span class="sxs-lookup"><span data-stu-id="a8398-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="a8398-113">Verwenden New-AzMapsAccountKey (New-AzMapsAccountKey.md), um einen Schlüssel neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8398-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="a8398-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8398-114">EXAMPLES</span></span>

### <span data-ttu-id="a8398-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8398-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a8398-116">Gibt die Schlüssel für das Konto mit dem Namen MyAccount in der Ressourcengruppe MyResourceGroup zurück.</span><span class="sxs-lookup"><span data-stu-id="a8398-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a8398-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8398-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="a8398-118">Gibt die Schlüssel für das angegebene Azure Maps-Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="a8398-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="a8398-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a8398-119">PARAMETERS</span></span>

### <span data-ttu-id="a8398-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8398-120">-DefaultProfile</span></span>
<span data-ttu-id="a8398-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8398-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8398-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8398-122">-InputObject</span></span>
<span data-ttu-id="a8398-123">Kartenkonto aus Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="a8398-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8398-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a8398-124">-Name</span></span>
<span data-ttu-id="a8398-125">Karten-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="a8398-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8398-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8398-126">-ResourceGroupName</span></span>
<span data-ttu-id="a8398-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a8398-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8398-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8398-128">-ResourceId</span></span>
<span data-ttu-id="a8398-129">Ordnet "Account ResourceId" zu.</span><span class="sxs-lookup"><span data-stu-id="a8398-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8398-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8398-130">CommonParameters</span></span>
<span data-ttu-id="a8398-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8398-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8398-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8398-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8398-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8398-133">INPUTS</span></span>

### <span data-ttu-id="a8398-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a8398-134">System.String</span></span>

### <span data-ttu-id="a8398-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a8398-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="a8398-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8398-136">OUTPUTS</span></span>

### <span data-ttu-id="a8398-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a8398-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="a8398-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a8398-138">NOTES</span></span>

## <span data-ttu-id="a8398-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a8398-139">RELATED LINKS</span></span>
