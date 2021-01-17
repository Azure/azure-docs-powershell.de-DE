---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381169"
---
# <span data-ttu-id="2595c-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="2595c-101">Get-AzAttestation</span></span>

## <span data-ttu-id="2595c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2595c-102">SYNOPSIS</span></span>
<span data-ttu-id="2595c-103">Ruft einen Nachweis ab.</span><span class="sxs-lookup"><span data-stu-id="2595c-103">Gets an attestation.</span></span>

## <span data-ttu-id="2595c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2595c-104">SYNTAX</span></span>

### <span data-ttu-id="2595c-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2595c-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2595c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2595c-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2595c-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="2595c-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2595c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2595c-108">DESCRIPTION</span></span>
<span data-ttu-id="2595c-109">Das Get-AzAttestation cmdlet ruft Informationen zum Nachweis in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2595c-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="2595c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2595c-110">EXAMPLES</span></span>

### <span data-ttu-id="2595c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2595c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="2595c-112">Pshtest des *Nachweisanbieters* in der *Ressourcengruppe psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="2595c-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="2595c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2595c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="2595c-114">Alle verfügbaren Standardanbieter für Nachweise erhalten</span><span class="sxs-lookup"><span data-stu-id="2595c-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="2595c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2595c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="2595c-116">Attestation Default Provider from Location *East US 2*</span><span class="sxs-lookup"><span data-stu-id="2595c-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="2595c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2595c-117">PARAMETERS</span></span>

### <span data-ttu-id="2595c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2595c-118">-DefaultProfile</span></span>
<span data-ttu-id="2595c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2595c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2595c-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="2595c-120">-DefaultProvider</span></span>
<span data-ttu-id="2595c-121">Gibt dies die Anforderung an einen Standardprüfanbieter an.</span><span class="sxs-lookup"><span data-stu-id="2595c-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2595c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="2595c-122">-Location</span></span>
<span data-ttu-id="2595c-123">Gibt den Speicherort des Standard nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="2595c-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2595c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2595c-124">-Name</span></span>
<span data-ttu-id="2595c-125">Nachweisname.</span><span class="sxs-lookup"><span data-stu-id="2595c-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2595c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2595c-126">-ResourceGroupName</span></span>
<span data-ttu-id="2595c-127">Gibt den Namen der Ressourcengruppe an, die dem abgefragten Nachweis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2595c-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2595c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2595c-128">-ResourceId</span></span>
<span data-ttu-id="2595c-129">Gibt den Namen der ResourceID an, die dem abgefragten Nachweis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2595c-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="2595c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2595c-130">CommonParameters</span></span>
<span data-ttu-id="2595c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2595c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2595c-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2595c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2595c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2595c-133">INPUTS</span></span>

### <span data-ttu-id="2595c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2595c-134">System.String</span></span>

## <span data-ttu-id="2595c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2595c-135">OUTPUTS</span></span>

### <span data-ttu-id="2595c-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="2595c-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="2595c-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2595c-137">NOTES</span></span>

## <span data-ttu-id="2595c-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2595c-138">RELATED LINKS</span></span>
