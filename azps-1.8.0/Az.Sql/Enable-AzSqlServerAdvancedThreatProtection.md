---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659263"
---
# <span data-ttu-id="ec194-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ec194-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="ec194-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec194-102">SYNOPSIS</span></span>
<span data-ttu-id="ec194-103">Ermöglicht erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="ec194-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="ec194-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec194-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec194-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec194-105">DESCRIPTION</span></span>
<span data-ttu-id="ec194-106">Das Cmdlet **enable-AzSqlServerAdvancedThreatProtection** ermöglicht erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="ec194-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="ec194-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec194-107">EXAMPLES</span></span>

### <span data-ttu-id="ec194-108">Beispiel 1: Aktivieren von erweitertem Bedrohungsschutz für Server</span><span class="sxs-lookup"><span data-stu-id="ec194-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="ec194-109">Beispiel 2 – Aktivieren des erweiterten Bedrohungsschutzes für Server von Serverressourcen</span><span class="sxs-lookup"><span data-stu-id="ec194-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="ec194-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec194-110">PARAMETERS</span></span>

### <span data-ttu-id="ec194-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec194-111">-DefaultProfile</span></span>
<span data-ttu-id="ec194-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec194-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec194-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ec194-113">-InputObject</span></span>
<span data-ttu-id="ec194-114">Das Serverobjekt, das mit der erweiterten Bedrohungsschutz Richtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="ec194-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="ec194-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec194-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec194-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec194-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec194-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="ec194-117">-ServerName</span></span>
<span data-ttu-id="ec194-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="ec194-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="ec194-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec194-119">-Confirm</span></span>
<span data-ttu-id="ec194-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec194-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec194-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec194-121">-WhatIf</span></span>
<span data-ttu-id="ec194-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec194-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec194-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec194-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec194-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec194-124">CommonParameters</span></span>
<span data-ttu-id="ec194-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec194-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec194-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec194-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec194-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec194-127">INPUTS</span></span>

### <span data-ttu-id="ec194-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ec194-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ec194-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ec194-129">System.String</span></span>

## <span data-ttu-id="ec194-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec194-130">OUTPUTS</span></span>

### <span data-ttu-id="ec194-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ec194-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="ec194-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec194-132">NOTES</span></span>

## <span data-ttu-id="ec194-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec194-133">RELATED LINKS</span></span>
