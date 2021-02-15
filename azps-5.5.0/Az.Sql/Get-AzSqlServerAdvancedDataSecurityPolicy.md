---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158284"
---
# <span data-ttu-id="cbcb4-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="cbcb4-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="cbcb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcb4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcb4-103">Ruft die Advanced Data Security-Richtlinie eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="cbcb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbcb4-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcb4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbcb4-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcb4-106">Das **Cmdlet "Get-AzSqlServerAdvancedDataSecurityPolicy"** ruft die Advanced Data Security-Richtlinie eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="cbcb4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbcb4-107">EXAMPLES</span></span>

### <span data-ttu-id="cbcb4-108">Beispiel 1: Ruft advanced Data Security für Server ab</span><span class="sxs-lookup"><span data-stu-id="cbcb4-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="cbcb4-109">Beispiel 2: Ruft die advanced Data Security des Servers von einer Serverressource ab.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="cbcb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbcb4-110">PARAMETERS</span></span>

### <span data-ttu-id="cbcb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcb4-111">-DefaultProfile</span></span>
<span data-ttu-id="cbcb4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbcb4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbcb4-113">-InputObject</span></span>
<span data-ttu-id="cbcb4-114">Das Serverobjekt, das für den Richtlinienvorgang "Advanced Data Security" verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="cbcb4-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcb4-115">-ResourceGroupName</span></span>
<span data-ttu-id="cbcb4-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb4-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbcb4-117">-ServerName</span></span>
<span data-ttu-id="cbcb4-118">SQL Den Namen des Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-118">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcb4-119">CommonParameters</span></span>
<span data-ttu-id="cbcb4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcb4-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbcb4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcb4-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbcb4-122">INPUTS</span></span>

### <span data-ttu-id="cbcb4-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cbcb4-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cbcb4-124">System.String</span><span class="sxs-lookup"><span data-stu-id="cbcb4-124">System.String</span></span>

## <span data-ttu-id="cbcb4-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbcb4-125">OUTPUTS</span></span>

### <span data-ttu-id="cbcb4-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cbcb4-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="cbcb4-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cbcb4-127">NOTES</span></span>

## <span data-ttu-id="cbcb4-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cbcb4-128">RELATED LINKS</span></span>
