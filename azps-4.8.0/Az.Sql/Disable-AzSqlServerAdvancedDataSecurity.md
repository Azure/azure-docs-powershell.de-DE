---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174144"
---
# <span data-ttu-id="f4805-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f4805-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="f4805-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4805-102">SYNOPSIS</span></span>
<span data-ttu-id="f4805-103">Deaktiviert die erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="f4805-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f4805-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4805-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4805-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4805-105">DESCRIPTION</span></span>
<span data-ttu-id="f4805-106">Das Cmdlet **Disable-AzSqlServerAdvancedDataSecurity** deaktiviert die erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="f4805-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f4805-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4805-107">EXAMPLES</span></span>

### <span data-ttu-id="f4805-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4805-108">Example 1</span></span>
### <span data-ttu-id="f4805-109">Beispiel 2: Deaktivieren der erweiterten Server Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="f4805-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="f4805-110">Beispiel 3: Deaktivieren der erweiterten Server-Datensicherheit von Serverressourcen</span><span class="sxs-lookup"><span data-stu-id="f4805-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="f4805-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4805-111">PARAMETERS</span></span>

### <span data-ttu-id="f4805-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4805-112">-DefaultProfile</span></span>
<span data-ttu-id="f4805-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4805-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4805-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4805-114">-InputObject</span></span>
<span data-ttu-id="f4805-115">Das Serverobjekt, das mit der erweiterten Datensicherheitsrichtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f4805-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="f4805-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4805-116">-ResourceGroupName</span></span>
<span data-ttu-id="f4805-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4805-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4805-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="f4805-118">-ServerName</span></span>
<span data-ttu-id="f4805-119">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="f4805-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="f4805-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4805-120">-Confirm</span></span>
<span data-ttu-id="f4805-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4805-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4805-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4805-122">-WhatIf</span></span>
<span data-ttu-id="f4805-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4805-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4805-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4805-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4805-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4805-125">CommonParameters</span></span>
<span data-ttu-id="f4805-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4805-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4805-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4805-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4805-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4805-128">INPUTS</span></span>

### <span data-ttu-id="f4805-129">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f4805-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f4805-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4805-130">System.String</span></span>

## <span data-ttu-id="f4805-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4805-131">OUTPUTS</span></span>

### <span data-ttu-id="f4805-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f4805-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="f4805-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4805-133">NOTES</span></span>

## <span data-ttu-id="f4805-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4805-134">RELATED LINKS</span></span>
