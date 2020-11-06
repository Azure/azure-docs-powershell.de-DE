---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 9b51a9e835962ea1715a458ace1ab02202068e30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499322"
---
# <span data-ttu-id="5c676-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c676-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="5c676-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c676-102">SYNOPSIS</span></span>
<span data-ttu-id="5c676-103">Entfernt die Bedrohungs Erkennungsrichtlinie aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5c676-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c676-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c676-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c676-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c676-105">DESCRIPTION</span></span>
<span data-ttu-id="5c676-106">Das Cmdlet **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** entfernt die Bedrohungs Erkennungsrichtlinie aus einer AzureAzure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5c676-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="5c676-107">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren, aus der dieses Cmdlet die Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="5c676-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="5c676-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c676-108">EXAMPLES</span></span>

### <span data-ttu-id="5c676-109">Beispiel 1: Entfernen einer Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="5c676-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5c676-110">Dieser Befehl entfernt die Richtlinie für die Bedrohungserkennung aus einer Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="5c676-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="5c676-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c676-111">PARAMETERS</span></span>

### <span data-ttu-id="5c676-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c676-112">-DatabaseName</span></span>
<span data-ttu-id="5c676-113">Gibt den Namen einer Datenbank an, in der die Bedrohungs Erkennungsrichtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c676-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c676-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c676-114">-DefaultProfile</span></span>
<span data-ttu-id="5c676-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5c676-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c676-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c676-116">-PassThru</span></span>
<span data-ttu-id="5c676-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c676-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c676-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5c676-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c676-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c676-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c676-120">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="5c676-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="5c676-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="5c676-121">-ServerName</span></span>
<span data-ttu-id="5c676-122">Gibt den Namen eines Servers an, auf dem die Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c676-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c676-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c676-123">-Confirm</span></span>
<span data-ttu-id="5c676-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c676-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c676-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c676-125">-WhatIf</span></span>
<span data-ttu-id="5c676-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c676-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c676-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c676-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c676-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c676-128">CommonParameters</span></span>
<span data-ttu-id="5c676-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c676-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c676-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c676-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c676-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c676-131">INPUTS</span></span>

### <span data-ttu-id="5c676-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c676-132">System.String</span></span>

## <span data-ttu-id="5c676-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c676-133">OUTPUTS</span></span>

### <span data-ttu-id="5c676-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5c676-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="5c676-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c676-135">NOTES</span></span>

## <span data-ttu-id="5c676-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c676-136">RELATED LINKS</span></span>

[<span data-ttu-id="5c676-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5c676-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


