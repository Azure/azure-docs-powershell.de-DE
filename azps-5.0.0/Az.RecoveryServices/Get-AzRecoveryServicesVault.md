---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179691"
---
# <span data-ttu-id="fd007-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fd007-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="fd007-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd007-102">SYNOPSIS</span></span>

<span data-ttu-id="fd007-103">Ruft eine Liste der Vaults für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="fd007-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="fd007-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd007-104">SYNTAX</span></span>

### <span data-ttu-id="fd007-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd007-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd007-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd007-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd007-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd007-107">DESCRIPTION</span></span>

<span data-ttu-id="fd007-108">Das Cmdlet " **Get-AzRecoveryServicesVault** " Ruft eine Liste der Wiederherstellungsdienste-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fd007-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="fd007-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd007-109">EXAMPLES</span></span>

### <span data-ttu-id="fd007-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd007-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="fd007-111">Abrufen der Liste des Tresors im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="fd007-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="fd007-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd007-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="fd007-113">Abrufen der Liste des Tresors in der Gruppe "Ressource" im ausgewählten Abonnement</span><span class="sxs-lookup"><span data-stu-id="fd007-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="fd007-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fd007-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="fd007-115">Abrufen des Tresors in der Ressourcengruppe mit dem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="fd007-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="fd007-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd007-116">PARAMETERS</span></span>

### <span data-ttu-id="fd007-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd007-117">-DefaultProfile</span></span>

<span data-ttu-id="fd007-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd007-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd007-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fd007-119">-Name</span></span>

<span data-ttu-id="fd007-120">Gibt den Namen des zu abfragenden Tresors an.</span><span class="sxs-lookup"><span data-stu-id="fd007-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd007-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd007-121">-ResourceGroupName</span></span>

<span data-ttu-id="fd007-122">Gibt den Namen der Azure-Ressourcengruppe an, aus der das angegebene Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd007-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd007-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd007-123">-Tag</span></span>

<span data-ttu-id="fd007-124">Gibt die zu abfragenden Tags an</span><span class="sxs-lookup"><span data-stu-id="fd007-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd007-125">-Tagname</span><span class="sxs-lookup"><span data-stu-id="fd007-125">-TagName</span></span>

<span data-ttu-id="fd007-126">Gibt den Schlüssel des zu abfragenden Transponders an</span><span class="sxs-lookup"><span data-stu-id="fd007-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd007-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="fd007-127">-TagValue</span></span>

<span data-ttu-id="fd007-128">Gibt den Wert der zu abfragenden Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="fd007-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd007-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd007-129">CommonParameters</span></span>
<span data-ttu-id="fd007-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd007-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd007-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd007-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd007-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd007-132">INPUTS</span></span>

### <span data-ttu-id="fd007-133">Keine</span><span class="sxs-lookup"><span data-stu-id="fd007-133">None</span></span>

## <span data-ttu-id="fd007-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd007-134">OUTPUTS</span></span>

### <span data-ttu-id="fd007-135">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="fd007-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="fd007-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd007-136">NOTES</span></span>
<span data-ttu-id="fd007-137">Get-AzRecoveryServicesVault in der alten Version von AZ. RecoveryServices (<= 2.10.0) können nicht mit AZ. Accounts (>= 1.8.1) aufgrund fehlerhafter Assemblyverweise funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fd007-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="fd007-138">Wenn Sie die neuesten AZ-oder AZ.-Konten verwenden, muss das Modul AZ. RecoveryServices auf 2.11.0 oder höher aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fd007-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="fd007-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd007-139">RELATED LINKS</span></span>

[<span data-ttu-id="fd007-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fd007-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="fd007-141">Neu – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fd007-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="fd007-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fd007-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
