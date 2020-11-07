---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659162"
---
# <span data-ttu-id="fa4ee-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa4ee-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="fa4ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4ee-103">Ruft erweiterte Bedrohungsschutz Richtlinien eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="fa4ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa4ee-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa4ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4ee-106">Das Cmdlet " **Get-AzSqlServerAdvancedThreatProtectionPolicy** " retrives die erweiterte Bedrohungsschutz Richtlinie eines Servers.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="fa4ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa4ee-107">EXAMPLES</span></span>

### <span data-ttu-id="fa4ee-108">Beispiel 1 – Ruft den erweiterten Server-Bedrohungsschutz ab</span><span class="sxs-lookup"><span data-stu-id="fa4ee-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="fa4ee-109">Beispiel 2 – Ruft den erweiterten Schutz vor Bedrohungen durch Serverressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="fa4ee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa4ee-110">PARAMETERS</span></span>

### <span data-ttu-id="fa4ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4ee-111">-DefaultProfile</span></span>
<span data-ttu-id="fa4ee-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa4ee-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa4ee-113">-InputObject</span></span>
<span data-ttu-id="fa4ee-114">Das Serverobjekt, das mit der erweiterten Bedrohungsschutz Richtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="fa4ee-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="fa4ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="fa4ee-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa4ee-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="fa4ee-117">-ServerName</span></span>
<span data-ttu-id="fa4ee-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="fa4ee-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="fa4ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4ee-119">CommonParameters</span></span>
<span data-ttu-id="fa4ee-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4ee-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa4ee-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4ee-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa4ee-122">INPUTS</span></span>

### <span data-ttu-id="fa4ee-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fa4ee-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fa4ee-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fa4ee-124">System.String</span></span>

## <span data-ttu-id="fa4ee-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa4ee-125">OUTPUTS</span></span>

### <span data-ttu-id="fa4ee-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fa4ee-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="fa4ee-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa4ee-127">NOTES</span></span>

## <span data-ttu-id="fa4ee-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa4ee-128">RELATED LINKS</span></span>
