---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499358"
---
# <span data-ttu-id="695ce-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="695ce-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="695ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="695ce-102">SYNOPSIS</span></span>
<span data-ttu-id="695ce-103">Ruft erweiterte Bedrohungsschutz Richtlinien eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="695ce-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="695ce-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="695ce-105">DESCRIPTION</span></span>
<span data-ttu-id="695ce-106">Das Cmdlet " **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** " retrives die erweiterte Bedrohungsschutz Richtlinie eines Servers.</span><span class="sxs-lookup"><span data-stu-id="695ce-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="695ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="695ce-107">EXAMPLES</span></span>

### <span data-ttu-id="695ce-108">Beispiel 1 – Ruft den erweiterten Server-Bedrohungsschutz ab</span><span class="sxs-lookup"><span data-stu-id="695ce-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="695ce-109">Beispiel 2 – Ruft den erweiterten Schutz vor Bedrohungen durch Serverressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="695ce-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="695ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="695ce-110">PARAMETERS</span></span>

### <span data-ttu-id="695ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695ce-111">-DefaultProfile</span></span>
<span data-ttu-id="695ce-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="695ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695ce-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="695ce-113">-InputObject</span></span>
<span data-ttu-id="695ce-114">Das Serverobjekt, das mit der erweiterten Bedrohungsschutz Richtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="695ce-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="695ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="695ce-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="695ce-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="695ce-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="695ce-117">-ServerName</span></span>
<span data-ttu-id="695ce-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="695ce-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="695ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695ce-119">CommonParameters</span></span>
<span data-ttu-id="695ce-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695ce-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695ce-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="695ce-122">INPUTS</span></span>

### <span data-ttu-id="695ce-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="695ce-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="695ce-124">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="695ce-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="695ce-125">System. String</span><span class="sxs-lookup"><span data-stu-id="695ce-125">System.String</span></span>

## <span data-ttu-id="695ce-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="695ce-126">OUTPUTS</span></span>

### <span data-ttu-id="695ce-127">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="695ce-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="695ce-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="695ce-128">NOTES</span></span>

## <span data-ttu-id="695ce-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="695ce-129">RELATED LINKS</span></span>
