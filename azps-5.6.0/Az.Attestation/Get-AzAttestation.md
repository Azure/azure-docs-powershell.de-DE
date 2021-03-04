---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 73e51981dc57c4bc81f530f32b597c619b0bab78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935400"
---
# <span data-ttu-id="96c1a-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="96c1a-101">Get-AzAttestation</span></span>

## <span data-ttu-id="96c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="96c1a-103">Ruft eine Bestätigung ab.</span><span class="sxs-lookup"><span data-stu-id="96c1a-103">Gets an attestation.</span></span>

## <span data-ttu-id="96c1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96c1a-104">SYNTAX</span></span>

### <span data-ttu-id="96c1a-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="96c1a-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96c1a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96c1a-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c1a-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="96c1a-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96c1a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="96c1a-109">Das Get-AzAttestation-Cmdlet erhält Informationen über die Bescheinigung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96c1a-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="96c1a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="96c1a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96c1a-111">Example 1</span></span>
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

<span data-ttu-id="96c1a-112">Holen Sie sich den Testanbieter *pshtest* in der Ressourcengruppe *psh-test-rg*.</span><span class="sxs-lookup"><span data-stu-id="96c1a-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="96c1a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="96c1a-113">Example 2</span></span>
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

<span data-ttu-id="96c1a-114">Alle verfügbaren Standardanbieter für Die Bestätigung erhalten</span><span class="sxs-lookup"><span data-stu-id="96c1a-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="96c1a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="96c1a-115">Example 3</span></span>
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

<span data-ttu-id="96c1a-116">Holen Sie sich den Standardanbieter für Attestation von Location *East US 2*</span><span class="sxs-lookup"><span data-stu-id="96c1a-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="96c1a-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96c1a-117">PARAMETERS</span></span>

### <span data-ttu-id="96c1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c1a-118">-DefaultProfile</span></span>
<span data-ttu-id="96c1a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96c1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96c1a-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="96c1a-120">-DefaultProvider</span></span>
<span data-ttu-id="96c1a-121">Gibt an, dass dies die Anforderung an einen Standardprüfanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="96c1a-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="96c1a-122">-Location</span><span class="sxs-lookup"><span data-stu-id="96c1a-122">-Location</span></span>
<span data-ttu-id="96c1a-123">Gibt den Speicherort des Standardprüfanbieters an.</span><span class="sxs-lookup"><span data-stu-id="96c1a-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="96c1a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="96c1a-124">-Name</span></span>
<span data-ttu-id="96c1a-125">Name der Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="96c1a-125">Attestation Name.</span></span>

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

### <span data-ttu-id="96c1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="96c1a-127">Gibt den Namen der Ressourcengruppe an, die dem abgefragten Attest zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96c1a-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="96c1a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96c1a-128">-ResourceId</span></span>
<span data-ttu-id="96c1a-129">Gibt den Namen der ResourceID an, die dem abgefragten Attest zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96c1a-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="96c1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c1a-130">CommonParameters</span></span>
<span data-ttu-id="96c1a-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c1a-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c1a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c1a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96c1a-133">INPUTS</span></span>

### <span data-ttu-id="96c1a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="96c1a-134">System.String</span></span>

## <span data-ttu-id="96c1a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96c1a-135">OUTPUTS</span></span>

### <span data-ttu-id="96c1a-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="96c1a-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="96c1a-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96c1a-137">NOTES</span></span>

## <span data-ttu-id="96c1a-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96c1a-138">RELATED LINKS</span></span>
