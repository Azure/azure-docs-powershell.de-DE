---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/disable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: cc38d619b810f2567594c0c1020190c271dc9f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482005"
---
# <span data-ttu-id="728f4-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="728f4-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="728f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="728f4-102">SYNOPSIS</span></span>
<span data-ttu-id="728f4-103">Deaktiviert den erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="728f4-103">Disables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="728f4-104">SYNTAX</span></span>

```
Disable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="728f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="728f4-105">DESCRIPTION</span></span>
<span data-ttu-id="728f4-106">Das Cmdlet **Disable-AzureRmSqlServerAdvancedThreatProtection** deaktiviert den erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="728f4-106">The **Disable-AzureRmSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="728f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728f4-107">EXAMPLES</span></span>

### <span data-ttu-id="728f4-108">Beispiel 1 – Schutz vor erweiterten Bedrohungen durch Server deaktivieren</span><span class="sxs-lookup"><span data-stu-id="728f4-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="728f4-109">Beispiel 2 – deaktivieren Sie den erweiterten Schutz vor Bedrohungen durch Serverressourcen</span><span class="sxs-lookup"><span data-stu-id="728f4-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="728f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="728f4-110">PARAMETERS</span></span>

### <span data-ttu-id="728f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728f4-111">-DefaultProfile</span></span>
<span data-ttu-id="728f4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="728f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728f4-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="728f4-113">-InputObject</span></span>
<span data-ttu-id="728f4-114">Das Serverobjekt, das mit der erweiterten Bedrohungsschutz Richtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="728f4-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="728f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="728f4-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="728f4-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="728f4-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="728f4-117">-ServerName</span></span>
<span data-ttu-id="728f4-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="728f4-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="728f4-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="728f4-119">-Confirm</span></span>
<span data-ttu-id="728f4-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="728f4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728f4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728f4-121">-WhatIf</span></span>
<span data-ttu-id="728f4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="728f4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="728f4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="728f4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728f4-124">CommonParameters</span></span>
<span data-ttu-id="728f4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728f4-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728f4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728f4-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="728f4-127">INPUTS</span></span>

### <span data-ttu-id="728f4-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="728f4-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="728f4-129">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="728f4-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="728f4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="728f4-130">System.String</span></span>

## <span data-ttu-id="728f4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="728f4-131">OUTPUTS</span></span>

### <span data-ttu-id="728f4-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="728f4-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="728f4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="728f4-133">NOTES</span></span>

## <span data-ttu-id="728f4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="728f4-134">RELATED LINKS</span></span>
