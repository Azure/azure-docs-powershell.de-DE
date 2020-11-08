---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997442"
---
# <span data-ttu-id="5c660-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="5c660-101">Get-AzAttestation</span></span>

## <span data-ttu-id="5c660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c660-102">SYNOPSIS</span></span>
<span data-ttu-id="5c660-103">Ruft eine Bescheinigung ab.</span><span class="sxs-lookup"><span data-stu-id="5c660-103">Gets an attestation.</span></span>

## <span data-ttu-id="5c660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c660-104">SYNTAX</span></span>

### <span data-ttu-id="5c660-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c660-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c660-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c660-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c660-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c660-107">DESCRIPTION</span></span>
<span data-ttu-id="5c660-108">Das Get-AzAttestation-Cmdlet erhält Informationen zur Bescheinigung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c660-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="5c660-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c660-109">EXAMPLES</span></span>

### <span data-ttu-id="5c660-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c660-110">Example 1</span></span>
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

<span data-ttu-id="5c660-111">Besorgen Sie sich den Bestätigungs Anbieter *pshtest* in der Ressourcengruppe *PSH-Test-RG*.</span><span class="sxs-lookup"><span data-stu-id="5c660-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="5c660-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c660-112">PARAMETERS</span></span>

### <span data-ttu-id="5c660-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c660-113">-DefaultProfile</span></span>
<span data-ttu-id="5c660-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c660-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c660-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5c660-115">-Name</span></span>
<span data-ttu-id="5c660-116">Name der Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="5c660-116">Attestation Name.</span></span>

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

### <span data-ttu-id="5c660-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c660-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c660-118">Gibt den Namen der Ressourcengruppe an, die der abgefragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c660-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="5c660-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5c660-119">-ResourceId</span></span>
<span data-ttu-id="5c660-120">Gibt den Namen der Resourcen-Nr. an, die der Befragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c660-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="5c660-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c660-121">CommonParameters</span></span>
<span data-ttu-id="5c660-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c660-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c660-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c660-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c660-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c660-124">INPUTS</span></span>

### <span data-ttu-id="5c660-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5c660-125">System.String</span></span>

## <span data-ttu-id="5c660-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c660-126">OUTPUTS</span></span>

### <span data-ttu-id="5c660-127">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="5c660-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="5c660-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c660-128">NOTES</span></span>

## <span data-ttu-id="5c660-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c660-129">RELATED LINKS</span></span>
