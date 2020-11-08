---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165347"
---
# <span data-ttu-id="2187e-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="2187e-101">Get-AzAttestation</span></span>

## <span data-ttu-id="2187e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2187e-102">SYNOPSIS</span></span>
<span data-ttu-id="2187e-103">Ruft eine Bescheinigung ab.</span><span class="sxs-lookup"><span data-stu-id="2187e-103">Gets an attestation.</span></span>

## <span data-ttu-id="2187e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2187e-104">SYNTAX</span></span>

### <span data-ttu-id="2187e-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2187e-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2187e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2187e-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2187e-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="2187e-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2187e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2187e-108">DESCRIPTION</span></span>
<span data-ttu-id="2187e-109">Das Get-AzAttestation-Cmdlet erhält Informationen zur Bescheinigung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2187e-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="2187e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2187e-110">EXAMPLES</span></span>

### <span data-ttu-id="2187e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2187e-111">Example 1</span></span>
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

<span data-ttu-id="2187e-112">Besorgen Sie sich den Bestätigungs Anbieter *pshtest* in der Ressourcengruppe *PSH-Test-RG*.</span><span class="sxs-lookup"><span data-stu-id="2187e-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="2187e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2187e-113">Example 2</span></span>
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

<span data-ttu-id="2187e-114">Abrufen aller verfügbaren Bestätigungs Standardanbieter</span><span class="sxs-lookup"><span data-stu-id="2187e-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="2187e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2187e-115">Example 3</span></span>
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

<span data-ttu-id="2187e-116">Abrufen des Standardanbieters für Bescheinigungen von Standort *Ost-US 2*</span><span class="sxs-lookup"><span data-stu-id="2187e-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="2187e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2187e-117">PARAMETERS</span></span>

### <span data-ttu-id="2187e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2187e-118">-DefaultProfile</span></span>
<span data-ttu-id="2187e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2187e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2187e-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="2187e-120">-DefaultProvider</span></span>
<span data-ttu-id="2187e-121">Gibt an, dass es sich um die Anforderung an einen Standard Zertifizierungsanbieter handelt.</span><span class="sxs-lookup"><span data-stu-id="2187e-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="2187e-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="2187e-122">-Location</span></span>
<span data-ttu-id="2187e-123">Gibt den Speicherort des standardmäßigen Zertifizierungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="2187e-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="2187e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2187e-124">-Name</span></span>
<span data-ttu-id="2187e-125">Name der Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="2187e-125">Attestation Name.</span></span>

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

### <span data-ttu-id="2187e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2187e-126">-ResourceGroupName</span></span>
<span data-ttu-id="2187e-127">Gibt den Namen der Ressourcengruppe an, die der abgefragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2187e-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="2187e-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2187e-128">-ResourceId</span></span>
<span data-ttu-id="2187e-129">Gibt den Namen der Resourcen-Nr. an, die der Befragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2187e-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="2187e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2187e-130">CommonParameters</span></span>
<span data-ttu-id="2187e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2187e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2187e-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2187e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2187e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2187e-133">INPUTS</span></span>

### <span data-ttu-id="2187e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2187e-134">System.String</span></span>

## <span data-ttu-id="2187e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2187e-135">OUTPUTS</span></span>

### <span data-ttu-id="2187e-136">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="2187e-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="2187e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2187e-137">NOTES</span></span>

## <span data-ttu-id="2187e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2187e-138">RELATED LINKS</span></span>
