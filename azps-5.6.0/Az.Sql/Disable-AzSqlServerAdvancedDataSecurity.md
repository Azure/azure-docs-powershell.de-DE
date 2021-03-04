---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926408"
---
# <span data-ttu-id="9d23b-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="9d23b-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="9d23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d23b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d23b-103">Deaktiviert Advanced Data Security auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="9d23b-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="9d23b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d23b-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d23b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d23b-105">DESCRIPTION</span></span>
<span data-ttu-id="9d23b-106">Das **Cmdlet Disable-AzSqlServerAdvancedDataSecurity** deaktiviert Advanced Data Security auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="9d23b-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="9d23b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d23b-107">EXAMPLES</span></span>

### <span data-ttu-id="9d23b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d23b-108">Example 1</span></span>
### <span data-ttu-id="9d23b-109">Beispiel 2: Deaktivieren der erweiterten Datensicherheit des Servers</span><span class="sxs-lookup"><span data-stu-id="9d23b-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="9d23b-110">Beispiel 3: Deaktivieren der erweiterten Serverdatensicherheit von der Serverressource</span><span class="sxs-lookup"><span data-stu-id="9d23b-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="9d23b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9d23b-111">PARAMETERS</span></span>

### <span data-ttu-id="9d23b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d23b-112">-DefaultProfile</span></span>
<span data-ttu-id="9d23b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d23b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d23b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d23b-114">-InputObject</span></span>
<span data-ttu-id="9d23b-115">Das Serverobjekt, das für den Vorgang der Erweiterten Datensicherheitsrichtlinie verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="9d23b-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="9d23b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d23b-116">-ResourceGroupName</span></span>
<span data-ttu-id="9d23b-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d23b-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="9d23b-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="9d23b-118">-ServerName</span></span>
<span data-ttu-id="9d23b-119">SQL Datenbankservername.</span><span class="sxs-lookup"><span data-stu-id="9d23b-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="9d23b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d23b-120">-Confirm</span></span>
<span data-ttu-id="9d23b-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d23b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d23b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d23b-122">-WhatIf</span></span>
<span data-ttu-id="9d23b-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d23b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d23b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d23b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d23b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d23b-125">CommonParameters</span></span>
<span data-ttu-id="9d23b-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d23b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d23b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d23b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d23b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d23b-128">INPUTS</span></span>

### <span data-ttu-id="9d23b-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9d23b-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="9d23b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9d23b-130">System.String</span></span>

## <span data-ttu-id="9d23b-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d23b-131">OUTPUTS</span></span>

### <span data-ttu-id="9d23b-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9d23b-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="9d23b-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9d23b-133">NOTES</span></span>

## <span data-ttu-id="9d23b-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9d23b-134">RELATED LINKS</span></span>
