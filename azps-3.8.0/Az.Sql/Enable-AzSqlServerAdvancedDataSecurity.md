---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 36efc8b3dfec4bcc126191d68c04c2cd5d071fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996282"
---
# <span data-ttu-id="f59bd-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="f59bd-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="f59bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f59bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f59bd-103">Ermöglicht erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="f59bd-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="f59bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59bd-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f59bd-105">DESCRIPTION</span></span>
<span data-ttu-id="f59bd-106">Das Cmdlet **enable-AzSqlServerAdvancedDataSecurity** ermöglicht erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="f59bd-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="f59bd-107">Advanced Data Security ist ein einheitliches Sicherheitspaket, das die Datenklassifizierung, die Gefährdungsbeurteilung und den erweiterten Bedrohungsschutz für Ihren Server umfasst.</span><span class="sxs-lookup"><span data-stu-id="f59bd-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="f59bd-108">(Es wird automatisch ein neues Speicherkonto zum Speichern von Sicherheitsrisikobewertungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f59bd-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="f59bd-109">Wenn zuvor ein Speicherkonto für diesen Zweck erstellt wurde, wird es stattdessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f59bd-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="f59bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f59bd-110">EXAMPLES</span></span>

### <span data-ttu-id="f59bd-111">Beispiel 1: Aktivieren der erweiterten Datensicherheit für Server</span><span class="sxs-lookup"><span data-stu-id="f59bd-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="f59bd-112">Beispiel 2 – Aktivieren der Server erweiterten Datensicherheit von der Server Ressource</span><span class="sxs-lookup"><span data-stu-id="f59bd-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="f59bd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f59bd-113">PARAMETERS</span></span>

### <span data-ttu-id="f59bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f59bd-114">-AsJob</span></span>
<span data-ttu-id="f59bd-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f59bd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f59bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59bd-116">-DefaultProfile</span></span>
<span data-ttu-id="f59bd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f59bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59bd-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="f59bd-118">-DeploymentName</span></span>
<span data-ttu-id="f59bd-119">Angeben eines benutzerdefinierten Namens für die erweiterte Bereitstellung von Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="f59bd-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59bd-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="f59bd-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="f59bd-121">Sicherheitsrisikobewertung nicht automatisch aktivieren (Dadurch wird kein Speicherkonto erstellt)</span><span class="sxs-lookup"><span data-stu-id="f59bd-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="f59bd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f59bd-122">-InputObject</span></span>
<span data-ttu-id="f59bd-123">Das Serverobjekt, das mit der erweiterten Datensicherheitsrichtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f59bd-123">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="f59bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="f59bd-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f59bd-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f59bd-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="f59bd-126">-ServerName</span></span>
<span data-ttu-id="f59bd-127">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="f59bd-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="f59bd-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f59bd-128">-Confirm</span></span>
<span data-ttu-id="f59bd-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f59bd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59bd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59bd-130">-WhatIf</span></span>
<span data-ttu-id="f59bd-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f59bd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59bd-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f59bd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59bd-133">CommonParameters</span></span>
<span data-ttu-id="f59bd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59bd-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59bd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59bd-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f59bd-136">INPUTS</span></span>

### <span data-ttu-id="f59bd-137">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f59bd-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f59bd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f59bd-138">System.String</span></span>

## <span data-ttu-id="f59bd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f59bd-139">OUTPUTS</span></span>

### <span data-ttu-id="f59bd-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f59bd-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="f59bd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f59bd-141">NOTES</span></span>

## <span data-ttu-id="f59bd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f59bd-142">RELATED LINKS</span></span>
