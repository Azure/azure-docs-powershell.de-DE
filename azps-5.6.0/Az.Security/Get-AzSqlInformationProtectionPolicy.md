---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936608"
---
# <span data-ttu-id="17651-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17651-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="17651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17651-102">SYNOPSIS</span></span>
<span data-ttu-id="17651-103">Ruft den effektiven Mandanten SQL Informationsschutzrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="17651-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="17651-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17651-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17651-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17651-105">DESCRIPTION</span></span>
<span data-ttu-id="17651-106">Ruft den effektiven Mandanten SQL Informationsschutzrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="17651-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="17651-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17651-107">EXAMPLES</span></span>

### <span data-ttu-id="17651-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17651-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="17651-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17651-109">PARAMETERS</span></span>

### <span data-ttu-id="17651-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17651-110">-AsJob</span></span>
<span data-ttu-id="17651-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17651-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17651-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17651-112">-DefaultProfile</span></span>
<span data-ttu-id="17651-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17651-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17651-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17651-114">CommonParameters</span></span>
<span data-ttu-id="17651-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17651-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17651-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17651-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17651-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17651-117">INPUTS</span></span>

### <span data-ttu-id="17651-118">System.string</span><span class="sxs-lookup"><span data-stu-id="17651-118">System.string</span></span>

## <span data-ttu-id="17651-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17651-119">OUTPUTS</span></span>

### <span data-ttu-id="17651-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="17651-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="17651-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17651-121">NOTES</span></span>

## <span data-ttu-id="17651-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17651-122">RELATED LINKS</span></span>
