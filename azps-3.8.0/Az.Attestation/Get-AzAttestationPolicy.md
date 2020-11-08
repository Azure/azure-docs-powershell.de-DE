---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997437"
---
# <span data-ttu-id="96326-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="96326-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="96326-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96326-102">SYNOPSIS</span></span>
<span data-ttu-id="96326-103">Ruft die Richtlinie eines Mandanten in Azure-Bescheinigung ab.</span><span class="sxs-lookup"><span data-stu-id="96326-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="96326-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96326-104">SYNTAX</span></span>

### <span data-ttu-id="96326-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96326-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96326-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96326-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96326-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96326-107">DESCRIPTION</span></span>
<span data-ttu-id="96326-108">Das Get-AzAttestationPolicy-Cmdlet ruft die Richtlinie eines Mandanten in Azure-Bescheinigung ab.</span><span class="sxs-lookup"><span data-stu-id="96326-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="96326-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96326-109">EXAMPLES</span></span>

### <span data-ttu-id="96326-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96326-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="96326-111">Ruft die Richtlinie für den Bestätigungs Anbieter *pshtest* für Tee-Typ *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="96326-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="96326-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="96326-112">PARAMETERS</span></span>

### <span data-ttu-id="96326-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96326-113">-DefaultProfile</span></span>
<span data-ttu-id="96326-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96326-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96326-115">-Name</span><span class="sxs-lookup"><span data-stu-id="96326-115">-Name</span></span>
<span data-ttu-id="96326-116">Gibt den Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="96326-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="96326-117">Dieses Cmdlet ruft die für den Mandanten beurkundete Richtlinie ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="96326-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="96326-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96326-118">-ResourceGroupName</span></span>
<span data-ttu-id="96326-119">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="96326-119">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96326-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="96326-120">-ResourceId</span></span>
<span data-ttu-id="96326-121">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="96326-121">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="96326-122">-Tee</span><span class="sxs-lookup"><span data-stu-id="96326-122">-Tee</span></span>
<span data-ttu-id="96326-123">Gibt einen Typ einer vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="96326-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="96326-124">Wir unterstützen vier Arten von Umgebungen: SgxEnclave, openenklave, CyResComponent und VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="96326-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96326-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96326-125">-Confirm</span></span>
<span data-ttu-id="96326-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96326-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96326-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96326-127">-WhatIf</span></span>
<span data-ttu-id="96326-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96326-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96326-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96326-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96326-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96326-130">CommonParameters</span></span>
<span data-ttu-id="96326-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96326-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96326-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96326-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96326-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96326-133">INPUTS</span></span>

### <span data-ttu-id="96326-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96326-134">System.String</span></span>

## <span data-ttu-id="96326-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96326-135">OUTPUTS</span></span>

### <span data-ttu-id="96326-136">Microsoft. Azure. Commands. Testat. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="96326-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="96326-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="96326-137">NOTES</span></span>

## <span data-ttu-id="96326-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96326-138">RELATED LINKS</span></span>
