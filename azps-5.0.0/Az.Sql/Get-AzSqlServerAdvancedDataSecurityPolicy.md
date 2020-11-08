---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180007"
---
# <span data-ttu-id="37a57-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="37a57-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="37a57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37a57-102">SYNOPSIS</span></span>
<span data-ttu-id="37a57-103">Ruft erweiterte Datensicherheitsrichtlinien eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="37a57-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="37a57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37a57-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37a57-105">DESCRIPTION</span></span>
<span data-ttu-id="37a57-106">Das Cmdlet " **Get-AzSqlServerAdvancedDataSecurityPolicy** " Ruft die erweiterte Datensicherheitsrichtlinie eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="37a57-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="37a57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37a57-107">EXAMPLES</span></span>

### <span data-ttu-id="37a57-108">Beispiel 1: Abrufen der erweiterten Server Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="37a57-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="37a57-109">Beispiel 2: Abrufen der erweiterten Datensicherheit des Servers von der Server Ressource</span><span class="sxs-lookup"><span data-stu-id="37a57-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="37a57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37a57-110">PARAMETERS</span></span>

### <span data-ttu-id="37a57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a57-111">-DefaultProfile</span></span>
<span data-ttu-id="37a57-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37a57-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a57-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37a57-113">-InputObject</span></span>
<span data-ttu-id="37a57-114">Das Serverobjekt, das mit der erweiterten Datensicherheitsrichtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="37a57-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="37a57-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a57-115">-ResourceGroupName</span></span>
<span data-ttu-id="37a57-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37a57-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="37a57-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="37a57-117">-ServerName</span></span>
<span data-ttu-id="37a57-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="37a57-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="37a57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a57-119">CommonParameters</span></span>
<span data-ttu-id="37a57-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a57-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37a57-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a57-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37a57-122">INPUTS</span></span>

### <span data-ttu-id="37a57-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="37a57-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="37a57-124">System. String</span><span class="sxs-lookup"><span data-stu-id="37a57-124">System.String</span></span>

## <span data-ttu-id="37a57-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37a57-125">OUTPUTS</span></span>

### <span data-ttu-id="37a57-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="37a57-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="37a57-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="37a57-127">NOTES</span></span>

## <span data-ttu-id="37a57-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37a57-128">RELATED LINKS</span></span>
