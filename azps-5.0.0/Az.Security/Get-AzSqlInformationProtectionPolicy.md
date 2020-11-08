---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176403"
---
# <span data-ttu-id="72abe-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="72abe-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="72abe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72abe-102">SYNOPSIS</span></span>
<span data-ttu-id="72abe-103">Ruft die effektive Mandanten-SQL-Informationsschutz Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="72abe-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="72abe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72abe-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72abe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72abe-105">DESCRIPTION</span></span>
<span data-ttu-id="72abe-106">Ruft die effektive Mandanten-SQL-Informationsschutz Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="72abe-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="72abe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72abe-107">EXAMPLES</span></span>

### <span data-ttu-id="72abe-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="72abe-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="72abe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="72abe-109">PARAMETERS</span></span>

### <span data-ttu-id="72abe-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72abe-110">-AsJob</span></span>
<span data-ttu-id="72abe-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="72abe-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72abe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72abe-112">-DefaultProfile</span></span>
<span data-ttu-id="72abe-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72abe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72abe-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72abe-114">CommonParameters</span></span>
<span data-ttu-id="72abe-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72abe-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72abe-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72abe-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72abe-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72abe-117">INPUTS</span></span>

### <span data-ttu-id="72abe-118">System. String</span><span class="sxs-lookup"><span data-stu-id="72abe-118">System.string</span></span>

## <span data-ttu-id="72abe-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72abe-119">OUTPUTS</span></span>

### <span data-ttu-id="72abe-120">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="72abe-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="72abe-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="72abe-121">NOTES</span></span>

## <span data-ttu-id="72abe-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72abe-122">RELATED LINKS</span></span>
