---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501585"
---
# <span data-ttu-id="f7c91-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7c91-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="f7c91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7c91-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c91-103">Ruft die Richtlinie für die Bedrohungserkennung für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="f7c91-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7c91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c91-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7c91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7c91-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c91-106">Das Cmdlet " **Get-AzureRmSqlServerThreatDetectionPolicy** " Ruft die Richtlinie für die Bedrohungserkennung eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="f7c91-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="f7c91-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren, für den dieses Cmdlet die Richtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="f7c91-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="f7c91-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7c91-108">EXAMPLES</span></span>

### <span data-ttu-id="f7c91-109">Beispiel 1: Abrufen der Bedrohungs Erkennungsrichtlinie für einen Server</span><span class="sxs-lookup"><span data-stu-id="f7c91-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="f7c91-110">Dieser Befehl ruft die Richtlinie für die Bedrohungserkennung für einen Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="f7c91-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="f7c91-111">Der Server ist der Ressourcengruppe ResourceGroup11 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f7c91-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f7c91-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7c91-112">PARAMETERS</span></span>

### <span data-ttu-id="f7c91-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c91-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7c91-114">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="f7c91-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="f7c91-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="f7c91-115">-ServerName</span></span>
<span data-ttu-id="f7c91-116">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="f7c91-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f7c91-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7c91-117">-Confirm</span></span>
<span data-ttu-id="f7c91-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7c91-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c91-119">-WhatIf</span></span>
<span data-ttu-id="f7c91-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7c91-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7c91-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7c91-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c91-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c91-122">-DefaultProfile</span></span>
<span data-ttu-id="f7c91-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7c91-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7c91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c91-124">CommonParameters</span></span>
<span data-ttu-id="f7c91-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c91-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c91-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c91-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7c91-127">INPUTS</span></span>

## <span data-ttu-id="f7c91-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7c91-128">OUTPUTS</span></span>

### <span data-ttu-id="f7c91-129">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f7c91-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="f7c91-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7c91-130">NOTES</span></span>

## <span data-ttu-id="f7c91-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7c91-131">RELATED LINKS</span></span>

[<span data-ttu-id="f7c91-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7c91-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="f7c91-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f7c91-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


