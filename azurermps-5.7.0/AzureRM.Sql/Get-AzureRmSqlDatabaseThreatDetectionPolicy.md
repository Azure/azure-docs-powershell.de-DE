---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498770"
---
# <span data-ttu-id="587f7-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="587f7-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="587f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="587f7-102">SYNOPSIS</span></span>
<span data-ttu-id="587f7-103">Ruft die Richtlinie für die Bedrohungserkennung für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="587f7-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="587f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="587f7-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="587f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="587f7-105">DESCRIPTION</span></span>
<span data-ttu-id="587f7-106">Das Cmdlet " **Get-AzureRmSqlDatabaseThreatDetectionPolicy** " Ruft die Bedrohungs Erkennungsrichtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="587f7-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="587f7-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren, für die dieses Cmdlet die Richtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="587f7-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="587f7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="587f7-108">EXAMPLES</span></span>

### <span data-ttu-id="587f7-109">Beispiel 1: Abrufen der Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="587f7-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="587f7-110">Dieser Befehl ruft die Richtlinie für die Bedrohungserkennung für eine Datenbank mit dem Namen database01 ab.</span><span class="sxs-lookup"><span data-stu-id="587f7-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="587f7-111">Die Datenbank befindet sich auf dem Server mit dem Namen Server01, der der Ressourcengruppe ResourceGroup11 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="587f7-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="587f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="587f7-112">PARAMETERS</span></span>

### <span data-ttu-id="587f7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="587f7-113">-DatabaseName</span></span>
<span data-ttu-id="587f7-114">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="587f7-114">Specifies the name of a database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587f7-115">-DefaultProfile</span></span>
<span data-ttu-id="587f7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="587f7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="587f7-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="587f7-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="587f7-119">-ServerName</span></span>
<span data-ttu-id="587f7-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="587f7-120">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="587f7-121">-Confirm</span></span>
<span data-ttu-id="587f7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="587f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="587f7-123">-WhatIf</span></span>
<span data-ttu-id="587f7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="587f7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="587f7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="587f7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587f7-126">CommonParameters</span></span>
<span data-ttu-id="587f7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587f7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587f7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587f7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="587f7-129">INPUTS</span></span>

###  
<span data-ttu-id="587f7-130">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="587f7-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="587f7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="587f7-131">OUTPUTS</span></span>

### <span data-ttu-id="587f7-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="587f7-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="587f7-133">Dieses Cmdlet gibt ein **Model. DatabaseThreatDetectionPolicyModel** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="587f7-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="587f7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="587f7-134">NOTES</span></span>

## <span data-ttu-id="587f7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="587f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="587f7-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="587f7-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



