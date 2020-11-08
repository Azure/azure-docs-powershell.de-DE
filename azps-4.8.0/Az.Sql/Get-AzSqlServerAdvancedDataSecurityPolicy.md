---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174123"
---
# <span data-ttu-id="ba7ae-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ba7ae-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ba7ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7ae-103">Ruft erweiterte Datensicherheitsrichtlinien eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="ba7ae-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="ba7ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7ae-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba7ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ba7ae-106">Das Cmdlet " **Get-AzSqlServerAdvancedDataSecurityPolicy** " Ruft die erweiterte Datensicherheitsrichtlinie eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="ba7ae-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="ba7ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba7ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ba7ae-108">Beispiel 1: Abrufen der erweiterten Server Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="ba7ae-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="ba7ae-109">Beispiel 2: Abrufen der erweiterten Datensicherheit des Servers von der Server Ressource</span><span class="sxs-lookup"><span data-stu-id="ba7ae-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="ba7ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba7ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ba7ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7ae-111">-DefaultProfile</span></span>
<span data-ttu-id="ba7ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba7ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba7ae-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba7ae-113">-InputObject</span></span>
<span data-ttu-id="ba7ae-114">Das Serverobjekt, das mit der erweiterten Datensicherheitsrichtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="ba7ae-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="ba7ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba7ae-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba7ae-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba7ae-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba7ae-117">-ServerName</span></span>
<span data-ttu-id="ba7ae-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="ba7ae-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="ba7ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7ae-119">CommonParameters</span></span>
<span data-ttu-id="ba7ae-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7ae-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba7ae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7ae-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba7ae-122">INPUTS</span></span>

### <span data-ttu-id="ba7ae-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ba7ae-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ba7ae-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ba7ae-124">System.String</span></span>

## <span data-ttu-id="ba7ae-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba7ae-125">OUTPUTS</span></span>

### <span data-ttu-id="ba7ae-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ba7ae-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="ba7ae-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba7ae-127">NOTES</span></span>

## <span data-ttu-id="ba7ae-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba7ae-128">RELATED LINKS</span></span>
