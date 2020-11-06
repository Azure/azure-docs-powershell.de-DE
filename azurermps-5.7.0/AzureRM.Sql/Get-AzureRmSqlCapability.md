---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 7d62a005455394dd1b00309adcf47bc639551a4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482698"
---
# <span data-ttu-id="9fe18-101">Get-AzureRmSqlCapability</span><span class="sxs-lookup"><span data-stu-id="9fe18-101">Get-AzureRmSqlCapability</span></span>

## <span data-ttu-id="9fe18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fe18-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe18-103">Ruft SQL-Datenbankfunktionen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9fe18-103">Gets SQL Database capabilities for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe18-104">SYNTAX</span></span>

### <span data-ttu-id="9fe18-105">FilterResults (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fe18-105">FilterResults (Default)</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe18-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="9fe18-106">DefaultResults</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe18-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe18-108">Das Cmdlet " **Get-AzureRmSqlCapability** " Ruft die Azure SQL-Datenbankfunktionen ab, die für das aktuelle Abonnement für einen Bereich verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9fe18-108">The **Get-AzureRmSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="9fe18-109">Wenn Sie die *ServerVersionName* -, *EditionName* -oder *ServiceObjectiveName* -Parameter angeben, gibt dieses Cmdlet die angegebenen Werte und ihre Vorgänger zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe18-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="9fe18-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fe18-110">EXAMPLES</span></span>

### <span data-ttu-id="9fe18-111">Beispiel 1: Abrufen von Funktionen für das aktuelle Abonnement für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="9fe18-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="9fe18-112">Dieser Befehl gibt die Funktionen für SQL-Datenbankinstanzen für das aktuelle Abonnement für die zentrale US-Region zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe18-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="9fe18-113">Beispiel 2: Abrufen von Standardfunktionen für das aktuelle Abonnement für einen Bereich</span><span class="sxs-lookup"><span data-stu-id="9fe18-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="9fe18-114">Dieser Befehl gibt die Standardfunktionen für SQL-Datenbanken für das aktuelle Abonnement in der zentralen US-Region zurück.</span><span class="sxs-lookup"><span data-stu-id="9fe18-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="9fe18-115">Beispiel 3: Abrufen von Details zu einem Dienst Ziel</span><span class="sxs-lookup"><span data-stu-id="9fe18-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="9fe18-116">Dieser Befehl ruft Standardfunktionen für SQL-Datenbanken für das angegebene Dienst Ziel für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9fe18-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="9fe18-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe18-117">PARAMETERS</span></span>

### <span data-ttu-id="9fe18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe18-118">-DefaultProfile</span></span>
<span data-ttu-id="9fe18-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9fe18-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fe18-120">– Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="9fe18-120">-Defaults</span></span>
<span data-ttu-id="9fe18-121">Gibt an, dass dieses Cmdlet nur Standardwerte erhält.</span><span class="sxs-lookup"><span data-stu-id="9fe18-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe18-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="9fe18-122">-EditionName</span></span>
<span data-ttu-id="9fe18-123">Gibt den Namen der Database Edition an, für die dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="9fe18-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe18-124">-Standortname</span><span class="sxs-lookup"><span data-stu-id="9fe18-124">-LocationName</span></span>
<span data-ttu-id="9fe18-125">Gibt den Namen des Speicherorts an, für den dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="9fe18-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="9fe18-126">Weitere Informationen finden Sie unter Azure-Bereiche https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="9fe18-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="9fe18-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="9fe18-127">-ServerVersionName</span></span>
<span data-ttu-id="9fe18-128">Gibt den Namen der Server Version an, für die dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="9fe18-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe18-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9fe18-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="9fe18-130">Gibt den Namen des Dienst Ziels an, für das dieses Cmdlet Funktionen erhält.</span><span class="sxs-lookup"><span data-stu-id="9fe18-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe18-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fe18-131">-Confirm</span></span>
<span data-ttu-id="9fe18-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fe18-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe18-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe18-133">-WhatIf</span></span>
<span data-ttu-id="9fe18-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe18-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe18-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fe18-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe18-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe18-136">CommonParameters</span></span>
<span data-ttu-id="9fe18-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe18-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe18-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe18-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe18-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fe18-139">INPUTS</span></span>

### <span data-ttu-id="9fe18-140">Keine</span><span class="sxs-lookup"><span data-stu-id="9fe18-140">None</span></span>
<span data-ttu-id="9fe18-141">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9fe18-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fe18-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fe18-142">OUTPUTS</span></span>

### <span data-ttu-id="9fe18-143">Microsoft.Azure.Commands.SQL.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="9fe18-143">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="9fe18-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fe18-144">NOTES</span></span>

## <span data-ttu-id="9fe18-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fe18-145">RELATED LINKS</span></span>
