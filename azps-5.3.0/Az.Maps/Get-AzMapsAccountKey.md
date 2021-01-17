---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468351"
---
# <span data-ttu-id="faa4b-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="faa4b-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="faa4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa4b-102">SYNOPSIS</span></span>
<span data-ttu-id="faa4b-103">Ruft die API-Schlüssel für ein Konto ab.</span><span class="sxs-lookup"><span data-stu-id="faa4b-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="faa4b-104">Diese Schlüssel sind der Authentifizierungsmechanismus, der bei nachfolgenden Aufrufen von Azure Maps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="faa4b-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="faa4b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faa4b-105">SYNTAX</span></span>

### <span data-ttu-id="faa4b-106">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="faa4b-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faa4b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="faa4b-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faa4b-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="faa4b-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faa4b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="faa4b-109">DESCRIPTION</span></span>
<span data-ttu-id="faa4b-110">Das Get-AzMapsAccountKey cmdlet ruft die API-Schlüssel für ein bereitgestelltes Azure -Kartenkonto ab.</span><span class="sxs-lookup"><span data-stu-id="faa4b-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="faa4b-111">Ein Azure -Karten-Konto verfügt über zwei API-Schlüssel: "Primär" und "Sekundär".</span><span class="sxs-lookup"><span data-stu-id="faa4b-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="faa4b-112">Die Schlüssel ermöglichen die Interaktion mit dem Azure Maps-Kontoendpunkt.</span><span class="sxs-lookup"><span data-stu-id="faa4b-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="faa4b-113">Verwenden New-AzMapsAccountKey (New-AzMapsAccountKey.md) zum erneuten Erstellen eines Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="faa4b-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="faa4b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="faa4b-114">EXAMPLES</span></span>

### <span data-ttu-id="faa4b-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faa4b-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="faa4b-116">Gibt die Schlüssel für das Konto mit dem Namen "MyAccount" in der Ressourcengruppe "MyResourceGroup" zurück.</span><span class="sxs-lookup"><span data-stu-id="faa4b-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="faa4b-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="faa4b-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="faa4b-118">Gibt die Schlüssel für das angegebene Azure -Kartenkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="faa4b-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="faa4b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faa4b-119">PARAMETERS</span></span>

### <span data-ttu-id="faa4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa4b-120">-DefaultProfile</span></span>
<span data-ttu-id="faa4b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faa4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa4b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa4b-122">-InputObject</span></span>
<span data-ttu-id="faa4b-123">Maps Account piped from Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="faa4b-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="faa4b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="faa4b-124">-Name</span></span>
<span data-ttu-id="faa4b-125">Kartenkontoname.</span><span class="sxs-lookup"><span data-stu-id="faa4b-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="faa4b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa4b-126">-ResourceGroupName</span></span>
<span data-ttu-id="faa4b-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="faa4b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="faa4b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faa4b-128">-ResourceId</span></span>
<span data-ttu-id="faa4b-129">Karten "Account ResourceId".</span><span class="sxs-lookup"><span data-stu-id="faa4b-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="faa4b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa4b-130">CommonParameters</span></span>
<span data-ttu-id="faa4b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa4b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa4b-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa4b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa4b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="faa4b-133">INPUTS</span></span>

### <span data-ttu-id="faa4b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="faa4b-134">System.String</span></span>

### <span data-ttu-id="faa4b-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="faa4b-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="faa4b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="faa4b-136">OUTPUTS</span></span>

### <span data-ttu-id="faa4b-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="faa4b-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="faa4b-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="faa4b-138">NOTES</span></span>

## <span data-ttu-id="faa4b-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="faa4b-139">RELATED LINKS</span></span>
