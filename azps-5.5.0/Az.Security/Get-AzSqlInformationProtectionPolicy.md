---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165956"
---
# <span data-ttu-id="8bdea-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8bdea-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="8bdea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bdea-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdea-103">Ruft den effektiven Mandanten SQL Informationsschutzrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="8bdea-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="8bdea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bdea-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bdea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bdea-105">DESCRIPTION</span></span>
<span data-ttu-id="8bdea-106">Ruft den effektiven Mandanten SQL Informationsschutzrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="8bdea-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="8bdea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bdea-107">EXAMPLES</span></span>

### <span data-ttu-id="8bdea-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8bdea-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="8bdea-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bdea-109">PARAMETERS</span></span>

### <span data-ttu-id="8bdea-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bdea-110">-AsJob</span></span>
<span data-ttu-id="8bdea-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8bdea-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bdea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdea-112">-DefaultProfile</span></span>
<span data-ttu-id="8bdea-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bdea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdea-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdea-114">CommonParameters</span></span>
<span data-ttu-id="8bdea-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdea-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdea-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bdea-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdea-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bdea-117">INPUTS</span></span>

### <span data-ttu-id="8bdea-118">System.string</span><span class="sxs-lookup"><span data-stu-id="8bdea-118">System.string</span></span>

## <span data-ttu-id="8bdea-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bdea-119">OUTPUTS</span></span>

### <span data-ttu-id="8bdea-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8bdea-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="8bdea-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8bdea-121">NOTES</span></span>

## <span data-ttu-id="8bdea-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8bdea-122">RELATED LINKS</span></span>
